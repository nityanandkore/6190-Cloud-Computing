# What are the tradeoffs with a serverless architecture?

### The serverless model is the easiest way for building scale-to-anything applications.

### Serverless applications typically cost less to run and are quicker to develop.

### Traffic spikes are not a problem but you should closely monitor usage.

### Low-latency and high-performance requirements are difficult to fulfill with a serverless architecture but this can be remedied with a serverless edge product

Cost forecast: serverless applications tend to cost less. However, higher traffic than usual can increase costs unexpectedly. Serverless applications have less of a flat rate so it’s important to monitor usage closely.

Latency: serverless functions can suffer from what is called the “cold start” problem, which is caused when cloud vendors deallocate resources after some time of inactivity. Infrequently used functions can have longer-than-usual startup times. Developers should take precautions to ensure that the functions are called periodically to keep the resources allocated and/or use a serverless edge product.

Resource Limits: serverless functions have limits in memory, CPU, and the execution duration. Consequently, a serverless architecture may not be a good fit for high-performance computing.

Observability: debugging, monitoring, and logging is difficult to do with serverless applications because functions are ephemeral. As serverless computing tooling matures, observability is expected to increase.

Lock-in: each cloud vendor has its own way of delivering serverless so migrating between clouds can be challenging. Some frameworks like the serverless framework alleviate this problem with a plugin structure that supports many clouds.

# How are the advantages to developing with Cloud9 ?

AWS Cloud9 is an IDE (that is integrated development environment) and operates in the cloud. It allows writing, running or debugging any code while using the web browser. Cloud9 has the code editor, a debugger and a terminal. Cloud9 contains some of the most used programming languages such as PHP and JavaScript among other languages; therefore, you won’t require installing programs on your devices before commencing on your projects. As cloud-based IDE, Cloud9 ensures you can work on your tasks from anywhere whether you are at home, office or on-site while accessing an internet –connected gadget. Cloud9 offers seamless experience in the development of serverless applications. Benefits of using Cloud9:

#### Flexible Browser Coding
#### Collaborative Coding
#### Develop Applications without the Need for a Server
#### Access AWS

# Post a screenshot of a lab where you had difficulty with a concept or learned something.
Learned how to create and use Lambda function
