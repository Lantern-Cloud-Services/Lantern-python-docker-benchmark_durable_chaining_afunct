# Lantern-python-docker-benchmark_durable_chaining_afunct

A Python implementation of an Azure chained durable function that takes a base integer and an exponential integer as query params.  The orchestrator function then instantiates an action function to perform the base value to the power the every integer from 2 to the exponential integer and sums the results of each execution, evaluating execution time required.  For example

http://127.0.0.1:7071/api/orchestrators/DurableOrchestration?base=3&exp=4

would perform an action function to produce the value of 

<code>3^2 = 9</code>
