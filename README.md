# Readme
An 8-bit computer that is equipped with a built-in 1kHz clock and is capable of basic assembly instructions such as ADD, LOAD, MOVE, and so on. This project is inspired by Ben Eater’s 8-bit computer, with simpler complexity and capability. The user can program the computer’s behavior using the EEPROM Programmer and by following the available opcodes.


![Full Assembly 1](https://github.com/JimpanzeeArchived/8-Bit-Computer-v2.0/assets/154708517/ffd64329-af78-4cdc-859f-1f89e615b7f0)
![Full_Assembly_1_NoWire](https://github.com/JimpanzeeArchived/8-Bit-Computer-v2.0/assets/154708517/c8f82b96-d1b7-43d2-82ca-91719793bc4b)
![Full_Assembly_2](https://github.com/JimpanzeeArchived/8-Bit-Computer-v2.0/assets/154708517/6adc8912-aa7b-4f7e-9184-56c522be8812)
![Full_Assembly_2_NoWire](https://github.com/JimpanzeeArchived/8-Bit-Computer-v2.0/assets/154708517/e91be7ef-5b75-4486-a5a1-bbefe22a5346)
![Full_Assembly_3_NoWire](https://github.com/JimpanzeeArchived/8-Bit-Computer-v2.0/assets/154708517/4390e364-a5bc-43f0-b426-f8e4f971ba8a)

#### Flow Diagram
![UML](https://github.com/JimpanzeeArchived/EEPROM-Programmer/assets/154708517/f827ec8d-cf36-44ad-87d7-6d04db121a2a)


#### CPU Module
The CPU aims to obtain users' instructions and output appropriate responses according to those instructions. The CPU consists of the instruction EEPROM and the main EEPROM. The main EEPROM is where the user can control the computer's behaviors by programming it using the EEPROM programmer. The user must provide an instruction from the OPCODE list, followed by an operand from 0-15. The user can program up to 16 instructions. The output of the main EEPROM is then fed onto the instruction EEPROM, which then outputs bits to control its eight-digit output to control the behavior of the computer. The data can be saved, moved, added, or loaded to the register depending on the instructions provided. 
![CPU](https://github.com/JimpanzeeArchived/8-Bit-Computer-v2.0/assets/154708517/eefc0b50-d68d-4cf0-8bd2-6dbdb0778cda)

#### Clock Module
The clock module is fed directly to the instruction clock.
![Clock](https://github.com/JimpanzeeArchived/8-Bit-Computer-v2.0/assets/154708517/b9aec771-fb50-4190-9557-a4f260da58e2)

#### Register A and Register SAVE Module
Register SAVE is used to store the operand values from the main EEPROM as soon as each instruction starts. The value can either be saved to register A or to load the main counter to implement the JUMP function.
Register A is fed directly to the input of the ALU, serving as a variable for the adder.
![RegARegSave](https://github.com/JimpanzeeArchived/8-Bit-Computer-v2.0/assets/154708517/61847414-49cf-47cb-8232-8ce534ba3702)

#### ALU
The ALU module consists of 2 adder modules and 2 selectors. The module processes the value it receives from register A and outputs an 8-bit number to the Seven Segment Display Module. 
![ALU](https://github.com/JimpanzeeArchived/8-Bit-Computer-v2.0/assets/154708517/2f07f200-852b-43a4-893e-695f64489977)

#### Seven Segment Display Module
The Seven Segment Display Module takes in an 8-bit number and outputs a 2-digit number.
![Seven_Segment_Disp](https://github.com/JimpanzeeArchived/8-Bit-Computer-v2.0/assets/154708517/8cd036ba-c3e0-4edd-b8c3-967db036fe1e)

#### Opcodes
The following shows a list of available opcodes:

![opcodes](https://github.com/JimpanzeeArchived/EEPROM-Programmer/assets/154708517/c280b302-ed33-4d8e-b138-7d5fdb731415)

#### Example
The video shows the computer programmed with the following instructions to add 3 and 4 repeatedly in an infinite loop. 
![example code](https://github.com/JimpanzeeArchived/EEPROM-Programmer/assets/154708517/ec1c0877-ec08-492f-95a0-58cb0d1bb426)
https://github.com/JimpanzeeArchived/8-Bit-Computer-v2.0/assets/154708517/88e93b67-46fd-44a7-b058-354273d4ef22
