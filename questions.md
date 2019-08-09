


## Qestions on knowledge distillation for beginners

- Knowledge Distillation vs Transfer Learning?
> I saw people use knowledge distillation instead of the transfer learning and also soft targets as the transferred information. However, KD is a method for Transfer Learning and soft targets just refers to the smoothed labels for the final cross entropy loss function of the student. I think we should be careful in our usage of these words.

- What is the best Temperature?
> Unfortunately, there is no direct method for getting the best temperature, however, the temperature is usually between 2 to 15. For example, you can test 5 for the first try.

- What is a good teacher?

> This is another open problem in knowledge distillation. Altough accuracy is crucial for the teacher, an ideal teacher will produce output probabilities exactly same as the GT labels which is not helpful for the student. In addition, when the teacher is much larger than the student, the soft targets will be too complex. In that case, a weaker teacher could lead to a better result for the student.

- Should the student always be smaller than the teacher?
> Not nececcerly, you can check the "Born Again Neural Networks" for example.

- Can the student surpass the teacher?

> Yes, it is possible when the student has enough capacity. 
