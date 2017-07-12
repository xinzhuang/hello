## Human Activity recognition based on sensor data on smart phones

### Data fusion Apps

- iOS: https://www.pgyer.com/mhar
- Android: https://fir.im/chn9

### How-to

1. Choose specific activity type on the default UI.
2. Lock the screen and get prepared.
3. Start to apply the activity we chose in step 1.
4. After 5 mins, stop.

### Data structure


	accelerate_x,accelerate_y,accelerate_z,gyroscope_x,gyroscope_y,gyroscope_z,
	gravity_x,gravity_y,gravity_z,magnetic_x,magnetic_y,magnetic_z,
	game_rotation_vector_x,game_rotation_vector_y,game_rotation_vector_z,
	orientation_x,orientation_y,orientation_z,
	world_accelerometer_x,world_accelerometer_y,world_accelerometer_z,
	light,pressure,temperature,timestamp

### Tips:

1. The sampling rate is 100Hz, lower down the frequency and re-sampling might be necessary.
2. Determine a proper slide window is important.
3. `world_accelerometer_x,world_accelerometer_y,world_accelerometer_z` is the accelerometer according to real world coordinate system, x is north, y is east, z is up.
4. Feature extraction is crutial for the model quality, please refer to 
	- https://github.com/blue-yonder/tsfresh
	- https://github.com/jindongwang/activityrecognition/tree/master/code
5. Classifer algorithm, please refer to https://github.com/TalkingData/Myna to use XGBoost or other ones you prefer.


