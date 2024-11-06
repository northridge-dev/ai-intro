## Picking a Project

- It should be something that interests you (but it needn't be a deep passion -- you won't have to work on this project for _that_ long).
- The most important constraint is availability of (**labeled**) data.
  - How much is enough? It's hard to know in advance. You may need to experiment.
- For this first project, let's stick close to what we've seen: image classification (or a problem that can be re-framed as an image classification problem).

## Tools

Unless you have good reason not to, let's try to use Kaggle notebooks and the FastAI wrapper around PyTorch.

## Process

1. Identify data:
   1. Where will you get your data?
   2. How will you get it into your environment (Kaggle notebook)?
   3. How will you label your data? It's common to use a file structure that mirrors your labels (e.g., a `bird` folder with all the bird images).
2. Create data loaders using the FastAI `DataBlocks` class. These are the data structures that will label, transform, and batch your data. See the examples in the Bird-Forest classifier or the Cat-NotCat classifier.
   1. Don't forget to set aside some of your data for model evaluation. For your data, does it make sense to randomly select what data will be set aside for testing? Or do you need to take a different approach to choosing what data to use for evaluation?
   2. Do you need to apply any transforms to your data? For example, you probably want to transform your images so they're a uniform size.
   3. (In a future iteration, you may want to play around with _data augmentation_, performing appropriate transforms on your data to synthetically generate more data. Maybe augmentation can improve the performance of a model even if you have a reasonably sized starting data set.)
3. Fine-tune your model. (No need to try training a model from scratch here.)
   1. Pick an appropriate pre-trained model. `resnet18` or `resnet34` are probably reasonable choices for image recognition / detection problems.
   2. Fine-tune the pre-trained model with the data you've prepared.
      1. `error_rate` is a good choice for the `metric`
      2. Start with a small number of training epochs (rounds) and see what sort of error rate it achieves before deciding to bump up the number of training epochs.
4. Investigate model performance and (maybe) clean your data. FastAI has [several tools](https://docs.fast.ai/interpret.html#classificationinterpretation) that can help you see where your classifications might be going wrong. Experiment a little. See what you can discover.
   1. `plot_confusion_matrix` will show you which categories your model is mixing up
   2. `plot_top_losses` will sort your images by _loss_ (a measurement of how far off the model's prediction is from the truth). It may help you discover some funky images that should be removed from your data set or misapplied labels.
   3. You can also tinker with the [`ImageClassifierCleaner`](https://docs.fast.ai/vision.widgets.html#imageclassifiercleaner), a widget that can help you identify and remove images from your data set.
5. Try retraining your model with your cleaned-up (or expanded) data set.
6. Repeat if you think you can squeeze out a little more error (and if you think squeezing out a little more error would be useful).

## Optional: Turn Your Model into a Web App

Follow [these instructions](https://colab.research.google.com/github/fastai/fastbook/blob/master/02_production.ipynb#scrollTo=Z3Y8NFpFJh4X) to export your model, build a web app _within a Python notebook_ (with the help of a few extensions), and deploy it on a service called Binder.

If there's interest and if I have time, we can explore a way to instead host these apps on northridge.dev.
