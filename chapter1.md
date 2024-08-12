# Chapter-1 Reliable, Scalable and Maintainable applications

An application needs to meet 2 kinds of requirements to be useful.

1. Functional requirements → ‘What it should do’
2. Non-functional requirements → like security, scalability, reliability, maintainability, compliance, compatibility


Some non-functional requirements :

Reliability

* Fault vs Failure : fault- single component deviation; failure-complete system failure
* how to make systems reliable?
    * redundancy
    * sandbox environments
    * thourough testing
    * detailed and clear monitoring
    * implement easy rollbacks during errors

Scalability

* Find the load parameter for your application to scale!
* Load- Usually, reads are frequent than writes; so it is better to do more work during writes, for less loading time during reads. 

Performance

* Response time vs latency - Latency is a subset of response time. While latency measures the delay before processing starts, response time measures the entire duration, including latency and the actual processing time.
* Response time requirements are measured in terms of 
    * (if) median (is 5ms) - p50 - (50% have response time <5ms and other 50% have >5ms)
    * percentiles - 95%, 99% and 99.9% (if is 1 sec) - p95, p99, p999 - (p95-95/100 req take <1sec and other 5 take >1sec)
* SLO vs SLA - Service Level Objectives SLOs drive the operational excellence of a service by setting performance targets, while Service Level aggrements SLAs define the contractual obligations and expectations between a service provider and its customers. Both are essential for delivering high-quality, reliable services.
* When several backend calls are needed to serve a request, it takes just a single slow backend request to slow down the entire end-user request. — Tail latency amplicifaction
* Head-of-Line(HOL) blocking and queuing delays are the most probable reasons for higher percentiles of response times

Maintainability

* To maintain any software systems without them turning into difficult to manage legacy systems, there are 3 main design principles 
    * Operability → maintaining and monitoring the existing system
    * Simplicity → make abstractions wherever possible
    * Evolvability/ plasticity / modifiability → ability to make changes in the system on a large scale

