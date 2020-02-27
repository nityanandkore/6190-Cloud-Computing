

# How could ASICs play an important role in Machine Learning going forward?

There are four major types of technology that can be used to accelerate the training and use of deep neural networks: CPUs, GPUs, FPGAs, and ASICs. The good old standby CPU has the advantage of being infinitely programmable, with decent but not stellar performance. It is used primarily in inference workloads where the trained Neural Network guides the computation to make accurate predictions about the input data item. FPGAs from Intel and Xilinx, on the other hand, offer excellent performance at very low power, but also offer more flexibility by allowing the designer to change the underlying hardware to best support changing software. FPGAs are used primarily in Machine Learning inference, video algorithms, and thousands of small-volume specialized applications. However, the skills needed to program the FPGA hardware are fairly hard to come by, and the performance of an FPGA will not approach that of a high-end GPU for certain workloads.

Technically, a GPU is an ASIC used for processing graphics algorithms. The difference is an ASIC offers an instruction set and libraries to allow the GPU to be programmed to operate on locally stored data—as an accelerator for many parallel algorithms. GPUs excel at performing matrix operations (primarily matrix multiplications, if you remember your high school math) that underlie graphics, AI, and many scientific algorithms. Basically, GPUs are very fast and relatively flexible.
The alternative is to design a custom ASIC dedicated to performing fixed operations extremely fast since the entire chip’s logic area can be dedicated to a set of narrow functions. In the case of the Google TPU, they lend themselves well to a high degree of parallelism, and processing neural networks is an “embarrassingly parallel” workload. Think of an ASIC as a drag racer; it can go very fast, but it can only carry one person in a straight line for a quarter mile. You couldn’t drive one around the block, or take it out on an oval racetrack.
Here’s the catch: designing an ASIC can be an expensive endeavor, costing many tens or even hundreds of millions of dollars and requiring a team of fairly expensive engineers. Paying for all that development means many tens or hundreds of thousands of chips are needed to amortize those expenses across the useful lifetime of the design (typically 2-3 years). Additionally, the chip will need to be updated frequently to keep abreast of new techniques and manufacturing processes. Finally, since the designers froze the logic early in the development process, they will be unable to react quickly when new ideas emerge in a fast moving field, such as AI. On the other hand, an FPGA (and to a limited extent even a GPU) can be reprogrammed to implement a new feature.

If you think about Google’s business, it has three attributes that likely led it to invest in custom silicon for AI. Examining these factors may be helpful in assessing other companies’ potential likelihood of making similar investments.

**Strategic Intent:**

Google has repeatedly stated that it has become an “AI First” company. In other words, AI technology has a strategic role across the entire business: Search, self-driving vehicles, Google Cloud, Google Home, and many other new and existing products and services. It, therefore, makes sense that Google would want to control its own hardware (TPU) accelerators and its own software framework (TensorFlow) on which they will build their products and services. The company is willing to invest to give themselves an edge over others with similar, albeit perhaps less ambitious, aspirations.

**Required Scale:**

Google’s computing infrastructure is the largest in the world, and that scale means that it may have the required volume needed to justify the significant costs of developing and maintaining its own hardware platform for AI acceleration. In fact, Google claims that the TPU saved the company from building another 12 datacenters to handle the AI load. Let’s do some sensitivity analysis to understand the likely scale required for a single ASIC cycle. For the sake of argument, let’s assume Google spent an Order of Magnitude of O($100M) including mask production, and that each chip will save them around O($1K). For reference, a single Cloud TPU chip at 45 TFLOPS potentially has a little more than 1/3rd the performance of a NVIDIA Volta GPU at a peak 120 TFLOPS, so you need 3 TPU chips to displace a high-end GPU. That implies Google can just about break even if they deploy an Order of Magnitude O(100K) TPUs, not accounting for the time value of money. That’s a lot of chips for most companies, even for Google. On the other hand, if it only cost Google O($60M) to develop the chip and TPU board, and they save O($2K) per chip, then they only need O(30K) chips to break even. Therefore a similar effort by another large datacenter may require an Order of Magnitude of O(30-100K) chips just to break even over a 2-3 year period).

**Importance of Google Cloud:**

Google execs can’t be satisfied to remain a distant 3rd in the global cloud computing market behind Amazon and Microsoft. They are investing a great deal in Google Cloud under the leadership of Diane Greene, and are now enjoying some of the fastest growth in the industry. Google could use the pricing power and performance of the Google Cloud TPU, along with the popularity of TensorFlow, as a potentially significant advantage in capturing market share for the development of machine learning in the cloud. However, it is important to note that Google says the use of their Cloud TPU would be priced at parity with a high-end GPU for cloud access. Google does not intend to sell the TPU outright.

Reference: http://www.moorinsightsstrategy.com/will-asic-chips-become-the-next-big-thing-in-ai/



# Find, run and extend a notebook in seedbank and share along with your comments on what you learned.

