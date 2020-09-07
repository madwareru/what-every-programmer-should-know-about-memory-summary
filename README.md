## what-every-programmer-should-know-about-memory-summary
### Short summary of the famous paper shedding a light on computer memory in a programmers perspective

#### Pt. I. Introduction
This part does not contain any useful info on the topic.

#### Pt. II. Commodity Hardware today
  0. There are several different ways to communicate between `RAM` and `CPU`, as well as
  periphery devices. Any time you require something from a `RAM`, in a generic scenario it should
  travel to you through a `north bridge`. Given a situation you need to communicate with some
  periphery such as some USB device or the hard drive, the data will travel through a `south bridge`
  and a `north bridge`(which is slower obviously). When the periphery device needs to access `RAM`,
  for the sake of performance it does it without the need in `CPU` but by utilizing a mechanism 
  known as direct memory access(`DMA`). It allows these devices to work relatively fast, but may cause 
  some losses in a speed of running programs. There is an architecture which lacks `north bridge` and 
  has memory controllers directly on `CPU` cores. In this situation CPU cores sometimes need to use other 
  cores as "proxies" to access data on a particular memory address. This approach is known as non-uniform 
  memory access or `NUMA`.

  1. There is two very distinct types of `RAM`, known as static(`SRAM`) and dynamic(`DRAM`).

  2. `SRAM` is desinged in a way that data in its unit is persistently available for the use
  which means it's potentially very fast. It's a smart scheme of six transistors. Read the paper
  for details on it.

  3. `DRAM`, on the other hand, is just a combination of a transistor and a capacitor, having data
  being stored in capacitor, and, as a result, providing a series of latencies needed to read and store data,
  as well as the need to recharge capacitor in some period of time. `DRAM` is much slower than `SRAM`.
  
  4. But we can't use `SRAM` everywhere, because:
      * It requires much more space on a die and its units cant pack on a die that well as `DRAM` memory units do
      * It's much more expensive (in orders of magnitude)
  
  5. As a result, we are facing compromise between performance and price: `SRAM` is used in `CPU caches` while `DRAM`
  is used for the ordinary `RAM`
  
#### Pt. III. CPU caches
To do

#### Pt. IV. Virtual Memory
To do

#### Pt. V. NUMA Support
To do

#### Pt. VI. What Programmers Can Do
To do

#### Pt. VII. Memory Performance tools
To do

#### Pt. VIII. Upcoming Technology
To do
