This is the communication part of the capstone project at University of Washington, Seattle.

Because of time constraint, the goal was to prove the concept of the project.
For the future, I recommend these changes:
1. currently we are using CLI for faster process. However, CLI is in ASCII, which is not ideal for data transfer. I recommend building with the API source code provided by OpenThread.
2. The wireless communication is done using UDP. Although UDP is instant, it may not be the best for "exact" data transfer. Consider other methods such as CoAP or TCP.

Unfinished tasks that were halted due to time constrait:
1. flow sensor's data was transmitted to the border router, however it couldn't be sent in the right format. int val needs to be converted to string and then sent using CLI command.
2. As of now, data collection and data transmission is merged on one microprocessor. Since STM32 has dual core, the two tasks need to be separated.


For code content,
[Communication] STM32_WPAN > App > "app_thread.c"
[Sensor ADC] Application > User > STM32_WPAN > "main.c"
	     Application > User > "MAX6675.c" and "MAX6675.h"
