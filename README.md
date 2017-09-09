# Tensorflow Retrain

## About

This is an example on how to use pre-existing TensorFlow models to retrain on your data. In this example, we use Inception which is an image classifier. You can train it on the existing images of different noodles type and then use images in the test directory to get the predictions.

## Setup

- Install tensorflow
- Put folders with images in "categories". The name of the folders will be the classifications.

## Training

``` bash
python retrain.py \
  --bottleneck_dir=bottlenecks \
  --how_many_training_steps=500 \
  --model_dir=inception \
  --summaries_dir=training_summaries/basic \
  --output_graph=retrained_graph.pb \
  --output_labels=retrained_labels.txt \
  --image_dir=categories
```

## Predicting

``` bash
python label_image.py <insert_file_path_to_predict_here>
```

## Credits

[Albert Padin](https://github.com/albertpadin)
