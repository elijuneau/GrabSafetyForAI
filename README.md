# GrabSafetyForAI
Grab Safety for AI but using Python version 2.7 (I think) + English translation and adding a few new modules.
So uhh, I got the main bulk of the code from here, mismashed with various code bits I added in myself (mostly version updates.) Shoutout to that great programmer-person.
https://github.com/FransdanaNadeak/GRAB-Data-Science/blob/master/GRAB%20-%20DATA%20SCIENCE%20(Safety).ipynb

Feature Engineering Ideas
The acceleration and gyroscope features are representative of the driver's behaviour (Z - vehicle bouncing, X - braking/ acceleration, Y - turning speed) with correction process, lateral, longitudinal and vertical movements of vehicle could be derived with these features.

Here lists some ideas for feature engineering processes:

Consider feature distance with speed & second
Consider feature speed for each axis with acceleration (xyz) with second
Consider feature radian for each axis with gyroscope (xyz) with second
Consider making axis interaction variables for both acceleration and gyroscope
Transform the accelerometer data: Vehicles move in one direction, only one of the axes will show large variation while others axes will typically have small fluctuation only. Therefore, you may summarise all three axes by finding the magnitude of acceleration using the formula: $\sqrt{ (acceleration_x)^{2} + (acceleration_y)^{2} + (acceleration_x)^{2}}$
Transform the gyroscope data: The distribution of gyroscope in all three axes are somewhat similar. Therefore, one idea is to use principal component analysis (PCA) to represent the triaxial gyroscope data in a lower dimension [What is PCA: https://towardsdatascience.com/a-complete-guide-to-principal-component-analysis-pca-in-machine-learning-664f34fc3e5a]

Reference links from previous challenge participants:

https://github.com/FransdanaNadeak/GRAB-Data-Science/blob/master/GRAB%20-%20DATA%20SCIENCE%20(Safety).ipynb
https://github.com/kfengtee/grab-aiforsea-safety/blob/master/documentation.ipynb
https://github.com/Toukenize/grab_aiforsea_safety

Problem Statements:

Which feature has a high impact on indicating dangerous trips?

How does the driving behaviour change over time (second) for normal trips and dangerous trips? What are the behaviour difference?

Given the telematics data for new trips,  derive a model to detect if the trip is a dangerous trip.
