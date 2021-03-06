# Tendies: TensorFlow Distributed Image Serving
A RESTful server application for image-based deep learning networks, allowing users to complete inference even on classified networks.
This server is compatible with models which input and output a float32 tensor representative of an image.

## Basic usage steps for a localhost server:
1. Clone the full_functionality directory to your machine.
2. Modify the example_usage function in ServerBuilder.py to instantiate your model instead of CycleGAN
3. Build your server with `python ServerBuilder.py --checkpoint_dir $(path) --protobuf_dir $(path) --image_size $(size)`
4. Run the server from bash with `tensorflow_model_server --rest_api_port=8501 --model_name=saved_model --model_base_path=$(path)`
5. Do inference on a directory of images with `python client.py --input_dir $(path)`

#### Please see minimum_working_example/tendies-tutorial.ipynb for an in-depth walkthrough of how this library works.
