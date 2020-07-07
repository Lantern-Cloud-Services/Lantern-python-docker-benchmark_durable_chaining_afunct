# Lantern-python-docker-benchmark_durable_chaining_afunct

A Python implementation of an Azure chained durable function that takes a base integer and an exponential integer as query params.  The orchestrator function then instantiates an action function to perform the base value to the power the every integer from 2 to the exponential integer and sums the results of each execution, evaluating execution time required.  For example

http://127.0.0.1:7071/api/orchestrators/DurableOrchestration?base=3&exp=4

would perform an action function to produce the value of 

<code>3^2 = 9</code>

<code>3^3 = 27</code>

<code>3^4 = 81</code>

resulting in a final sum of 

<code>117</code>

and a total time of ~.00621

With output similar to 

```
{
    "name": "DurableOrchestration",
    "instanceId": "71bf46aac01847679339104667fed288",
    "runtimeStatus": "Completed",
    "input": "{\"base\": \"3\", \"exp\": \"4\"}",
    "customStatus": null,
    "output": "With the input values base: 3, exp: 4 we calculated a total result of 117 in 0.006218910217285156 seconds",
    "createdTime": "2020-07-07T06:07:46Z",
    "lastUpdatedTime": "2020-07-07T06:07:48Z"
}
```
