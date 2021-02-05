# Data310 Informal Responses

## 1. In Laurence Maroney’s video, What is ML, he compares traditional programming with machine learning and argues that the main difference between the two is a reorientation of the rules, data and answers. According to Maroney, what is the difference between traditional programming and machine learning?

  Maroney describes the difference between traditional programming and machine learning being that instead of figuring out the rules that would give us answers like in traditional programming, with machine learning would feed a machine the answers and data and have it deduce the rules. Machine learning aims to match the data to its labels, becoming more accurate as it finds the pattern.
  
## 2.	With the first basic script that Maroney used to predict a value output from the model he estimated (he initially started with 10 that predicted ~31. Modify the predict function to produce the output for the value 7. Do this twice and provide both answers. Are they the same? Are they different? Why is this so?

Answer 1: [22.000025]
Answer 2: [22.000013]

  The answers were different when running the predict function between the first and second attempts. However, after the second attempt, the result remained the same. This could possibly be because the model is becoming more accurate in its estimates, and has solidified the pattern once it reaches a certain number of iterations.

## 3. •	Using the script you produced to predict housing price, take the provided six houses from Mathews, Virginia and train a neural net model that estimates the relationship between them. Based on this model, which of the six homes present a good deal? Which one is the worst deal? Justify your answer.


model = tf.keras.Sequential([keras.layers.Dense(units=1,input_shape=[1])])
model.compile(optimizer='sgd',loss='mean_squared_error')

xs = np.array([4.0, 3.0, 5.0, 4.0, 2.0 ,3],dtype=float)
ys = np.array([3.99, .97, 3.47, 2.89, 2.5, 2.29],dtype=float)
model.fit(xs,ys,epochs=500)

  From examining the results of the model, the second, third, fourth, and sixth houses present good deals, with the house on Holly Point having the best deal on a 3-bedroom house, saving about $142K off the predicted estimated house value based on the current model. The New Point 5-bedroom, Victorian 4-bedroom, and New Point comfort 3-bedroom houses present only moderate deals, saving about $10K on average off their predicted estimated values. However, the Church 4-bedroom house at $399K ultimately presents the worst deal, with the model estimating its value at only $298K; this makes the house overpriced by over $100,000.
