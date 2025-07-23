## EC2 Instance Types & Families
Amazon offers wide range of instance types and choosing them correctly helps in optimizing application performance
#### 1.	General Purpose instances:
```sh 
a.	Use this for non mission critical applications
b.	It offers equal ration of memory, cpu and network performances
c.	Use it for 
i.	Dev and test environments 
ii.	For small and medium databases 
iii.	For web applications
iv.	Virtual desktops
v.	Etc.
```
#### 2.	Compute Optimized Instances
```sh 
a.	It offers highest ratio of CPU
b.	Use this for applications whose dominant performance attribute is CPU.
```
#### 3.	Memory Optimized Instances
```sh 
a.	If offers highest ration of memory (RAM)
b.	Use it for memory intensive workloads (applications)
c.	Example use cases are
i.	SAP Hana (in-memory database)
ii.	Cache server
```
#### 4.	Storage Optimized Instances
```sh 
a.	Use it for applications that requires better IOPS (Input and output operations Per second)
b.	Databases typically write and read data to and from disk; these operations must be quick.
c.	You can use this to set up of data warehouses
5.	GPU 
a.	For video gaming
b.	For video and audio encoding.
```
AMD Processor
In AWS AMD processors offer better performance for a low price.

#### c5a.2xlarge
```sh 
C means compute optimized
5 means generation
a means AMD processor
2xlarge is the size
General Purpose Burstable Instance
→ All ‘t’ family instances in general purpose are burstable instances.
Let's take t2.micro, this offers 1 CPU and 1GB memory
When the CPU is idle it accumulates CPU credits. If your application needs more than 1 CPU it offers by consuming
CPU credits, after spending all credits it falls back to baseline performance.
(FAQ) Which type of instance are you using in your project?
c5a.large (Compute optimized
t3a.medium (General Purpose Burstable)
d3.xlarge (storage optimized)
r5a.large (For cache server)
```

#### Instance Families:
```sh 
Instance families
●	C – Compute optimized
●	D – Dense storage
●	F – FPGA
●	G – Graphics intensive
●	Hpc – High performance computing
●	I – Storage optimized
●	Im – Storage optimized with a one to four ratio of vCPU to memory
●	Is – Storage optimized with a one to six ratio of vCPU to memory
●	Inf – AWS Inferentia
●	M – General purpose
●	Mac – macOS
●	P – GPU accelerated
●	R – Memory optimized
●	T – Burstable performance
●	Trn – AWS Trainium
●	U – High memory
●	VT – Video transcoding
●	X – Memory intensive
Processor families
●	a – AMD processors
●	g – AWS Graviton processors
●	i – Intel processors
Additional capabilities
●	b – EBS optimized
●	d – Instance store volumes
●	n – Network and EBS optimized
●	e – Extra storage or memory
●	z – High performance
●	q – Qualcomm inference accelerators
●	flex – Flex instance
```
