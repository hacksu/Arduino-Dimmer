# Arduino-Dimmer

This project should guide you through the basics of setting up a circuit and controlling it with an Arduino. We'll cover topics such as ohm's law, voltage, current, and resistance, but more advanced topics will be left to another time and the reader's own discretion.

# Instructions

## It's alive

Take your Arduino and plug it into your laptop using a full sized USB cable. You should see the on led light up like this:

![Arduno Unio](https://lh3.googleusercontent.com/sUvDeIEGpGDZUC-w0v8qsllp8dG3f3zM03DdYGp4HzV9fAIGj8K00A33d6ti9Txl3hHpJ_zOwbrO20k-FJWtc4uDJmoPIRHABN4sbRhli86f3svsEBgfkSvQhO5yEA7RlieZnC_bm_GrlwzwdgGaaJT7kOjHnMuIgV5TXXSwSHmgAYosPE992H23Ez9NEupBZCi3J6Po5kIQ7GJPnW0iJx1YgPNZf6kI6lEMCTZi8CCLxUaDwY7gX4TcUji3R6hKGBeteUzjLQlyY6qspCg1kh9HthxZndsySTcuZjEqOB5AgVgWAmG9FI7iNwTiq9tDdBoqZ-Wr3e4QpZpUrdo8t6gJYv-vdA4eG13hpFre3-0zetF6UrBHEmBV5Zq7MTMOwqCTJ8bvGeQYBLd2GkPnjGI29zEUn7BXM9zjw4geKlnGzxAPN-nczYwEK8xXPQRJqZ-_ALG_MjI0IzskqOdOIJcxBl0IMGPvr9PVsLIa-UXszgZ9xSCZr5QMVQeWb7l37vNz6Tu7Nmpzou8nDrIicKyAN3lSCCfwPo-l5f705Etj1kYig5JsSW2CQKjJtMkLSSn5FQ=w1247-h935-no)

This means your Arduino has power and can be programmed via the IDE, we'll get back to that.

## Let there be light

Take out the breadboard and note how it's set up. At the top and bottom are two rows of holes labeled with a - and a +, these are meant for the positive and negative sides of the circuit and all the holes along these rows are hooked up under the plastic case. Similarly there are a group of columns labeled 1 through 30 and rows labeled a through e directly under these. This is a where most of this project will be constructed. Here each column is connected under the plastic. This lets us connected wires together without using trying to physically hold the wires together.

Let’s take a break to explain how electricity works in a circuit. People like to think of an electric circuit like water in a pipe. The water in this analogy flows from the positive side of the circuit to the negative side of the circuit. When the water is flowing there are two important variables to think about. How hard the water is pushing, the pressure, and how much is flowing through the pipe. There are two similar variables in a circuit. Voltage basically describes how much pressure is behind the electrons and current describes how many electrons are flowing through a wire. Most electronics works by keeping the voltage constant and letting the current vary as applications draw more and less current. Just like a pipe the current going through it can be restricted. We call the devices that do this resisters and they obey ohm's law. The total current in a circuit will equal the total voltage divided by the total resistance or I = V/R. The reason this is important is that we'll be using a device called an LED which can only take relatively low levels of current so we have to restrict the amount of current with a resistor. We have two resistors to choose from, but we'll be using the one without a red band.

LED stands for light emitting diode. The first two words make sense. It emits light, but diode may not be familiar to you. It refers to an LED's electronic characteristic. It's special because like all diodes it will only let electricity through in one direction. On an LED the positive end is marked by being longer.

So to make our circuit we will hook up the a wire from the 5V pin to our breadboard like this:

![Photo](https://lh3.googleusercontent.com/1QvwbbI7iZubcW7OOQ7iaUdHZSqC1kw8yhmH0HgEqIm8uEJ5JThdbkKq667p-CMbh13xAijloIVKP6xySTmFbIakcHk2Qq3njOUKR8dS8cM5nU6RMIBTk-pnXMu60BdJMHjG9ZxpzZeisJTsQwkHqGMAe4fOZ5azwVQiBT9UsQT32NU7lQyWuWylOBP86D79VEXcG_ySUHhM6y2ZQQ88S0ENDP1jN32CZRai_587tCISN0z7rBSdmI2WQ-aRhQaEAAkRktrydmMkp4f18q_0TFyMO0Bkn6RvJnY-xC3i7meHy11ACP9wZLNTxGVwase3kMFiVpmc9RvJ8stY7I9VDle0ZPze-TywnfBRkrYLoz96-vgtPhYptxCx2aHaOktjhZhf6MBOLR1VGOYHpuotLeqbbEZnOmY7HLV4IkcNll9GwnR9CKwW7DDDnNnJLY2EuwAL63YrUbPdj8e19xrnmdk6BVM0u3DAqT_IgQERfdTzJN-f1_QBV5y7XWaPpGSV0a3pu-FfbCJ3mRptN-NpZ2laFo2of1hkQ6p4twu2RKwMU6H9wsz_3_9wVRRLUXGXgikvcQ=w1264-h935-no)

Now we need to hook up the negative side of the circuit. We’ll hook up the ground pin to the - row on the top. Like this:

![Image](https://photos.google.com/share/AF1QipMBcczeYxiYsCME0iJaTzvbHGqMD8_pH914NMUlqfpzltCaO6E5RhdVxQ6scOQH0w/photo/AF1QipNUX85B_U9C0BCpg8fJfPDOvGPaJ2_4xfz-tFkJ?key=ZVNzbEZsVllJVElsVUt1OFk5TGE5dFBsOTJiX3hB)


Let’s add the resistor. Connect the resistor between the - row and a column, let’s do the one right next to the positive lead.

![example](https://lh3.googleusercontent.com/yg_OnrsiWH_L67u_fgSLXUZH7JRr-A_aK7gCOBv9V4ojFNNHSlqCbWJt8IbwJs7uAh4G5GHqAIQ-QIKw1ZSTRQhyNe6PTDIrXJ1Dugmb6hGXEHQAdBqVm3_Jj2CdICwGRdnboNyPiqTKt5VDs3ruASkW4Be7QDJqXlj_6WKmBKMBdLewH3HPTlb9m7YU8i5luqL1YjH3rh0IDmPNVfF3QELz1bxvdMC4L0hatL3usG2GBTo-te32hfdzGuo-fKtqWU_1LElsEy-c6kLBcjKL81bM49cToGAl2iz9WPdGLaGa3VrqlT4bATeMzR6yKixEf8I3xzddoQgyS8MFEPoHdjlBzJxIXJvgybm0kHUjHXciP6R_pGs9H8Ii5AepfWhb9u18e7MXkSFTUuDiI47gNZpC6Nm-uejif0rSrvhYmnQX5toyfK329T_gFgMi-61prhkGTfrj41-Ki8GgmVFH9uxJvzV1QlwmCGwaahQAVQpte3423a2Cqm0QFTQKRvxBCzeZjzteo-l6ckvhd8nPIL8EWssw2PTgR_eZRF86bBS-pscouqVIZgcpfBYYpIWFykaLjQ=w1264-h935-no)

Finally let’s put the LED in and watch it light up. Make sure to put the longer end in the positive column.

![LIGHT](https://lh3.googleusercontent.com/T-H7JXGB-w49C78Fs69HOroq_Igdj29HSK06fmSt-oQ0fr6Kh52wdbH7NY6OkHM1B6rFVdkp219iUa3WdhJjWl7eid2-_yMGLLfy83OZN_3L1aGSWgHqFBtj6FDPtBvFY0jHfh0aBahCuVo9GboKPXIGCzAZlrRoH0dIqzlF8M8lU7SxYRD2x9RFePqSlB8Qf_cq4rsx3JyeX7SfrR2Y6QsieI_9dGvUc1rHn58-_iXLmSyUdzFnnlL2oYFRIjw719ukXJR7HpMsB95nqISxOTQt4JLxcWtwrHQAMLMnMirPg_eVBG7fTEwFVQkmaPmblqKYvtKUIKZxLkhhSJhfNeBOCFQE1jrIFdmVC43oR1lBCnlTRDE28ZdsvhUC3CcEUL344l4_lQoVrighFRPCG6augh2vgwpMr0fzIsO4yJwBRDM7W3Y4bKpXNOtlP772B3PdbtDAGny1GWu3K7e_0fA7HXVTIKsO7m6mnAg9c-CRRLnc1X_U4LLY6b1Jr6iPyLEAKJqXmFw-r7uPtBNohEtj7QnJhbppe29a0svcN8me9LIAIK3HRPdtnBnf8zXEamMilg=w1264-h935-no)
