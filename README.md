# ModelMeter
<p align="center">
  <a href="https://pypi.org/project/model-meter"><img src="https://github.com/dayeondev/ModelMeter/assets/46081429/afff1336-57a6-45cb-8519-57cd59a03bb8" alt="ModelMeter" width="50%" height="50%"></a>
</p>
<p align="center">
    <em>Unrestricted class structure compatibility and focused throughput assessment for your model's performance evaluation</em>
</p>

## Requirements
Python 3.8+

## Installation
```console
pip install model-meter

---> 100%
```

## Example

### Create it

* Create a file `main.py` with:

``` python
from model_meter import ModelMeter
from ultralytics import YOLO

# Load the model
model = YOLO()

# Create the meter
meter = ModelMeter(model)

# Run the meter
throughput, avg_time_per_call = meter.measure(params=('./contents/dog.jpg',))

print(f'Throughput: {throughput} images/second')
print(f'Avg time per call: {avg_time_per_call} seconds')
```

### Run it

Run the script with:

```console
$ python main.py

...

Throughput: 14.794271662158552 images/second
Avg time per call: 0.0675937297107937 seconds
```

## License

This project is licensed under the terms of the MIT license.
