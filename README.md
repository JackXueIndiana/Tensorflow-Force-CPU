# Tensorflow-Force-CPU
Force TensorFlow to Use CPU in Version 1 &amp; 2


For TF 1, we can do this by setting
```python
config = tf.ConfigProto(device_count = {'GPU': 0})
```

For TF 2.0, we can do this by setting
```python
my_devices = tf.config.experimental.list_physical_devices(device_type='CPU')
tf.config.experimental.set_visible_devices(devices= my_devices, device_type='CPU')
```

For TF 2.1 and 2.2, we can do this by setting
```python
tf.config.set_visible_devices([], 'GPU')
```
