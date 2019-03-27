# Blockchain Performance
(Notes gathered)

## Important Blockchain Terms
* Consensus - Distributed process by which a network of nodes provide a guaranteed unique order of transactions and validates the blick of transactions.
* Commit - Point at which transaction is written to the database. Transactions are committed when the block has been circulated through the network and applied by all the nodes.
* Finality - Once a transaction is committed, it cannot be reversed, i.e. the point at which data once entered cannot be rolled back tot he previous state. There are different types of finality -
    * Voting Based Consensus (immediate finality)
    * Lottery Based Consensus with Probabilistic Finality
For testing purposes, formal threshholds of finality probability should be set up.
* Network Size - Network size is the number of validating nodes participating in consensus in the SUT. This count should not include observer nodes, or other nodes not actively participating in
both consensus and the validation of transactions.
* Query - Querying is the ability to run ad-hoc operations or searches against the dataset contained
within the blockchain. The SUT may not be built to execute these queries in a performant way. Any off-chain databases, or caches that support efficient querying, can still be measured. 

## Key Metrics
* Read Latency = Time when reply is recieved - Time when Read Request is submitted.
* Read Throughput = Total Read Operations/Total Time in Seconds
* Transaction Latency = The measurement includes the time from the point
that it is submitted to the point that the result is widely available in the network. This includes
the propagation time and any settling time due to the consensus mechanism in place
* Transaction Throughput = Total committed transactions / total time in seconds @ #committed nodes
Transaction throughput is the rate at which valid transactions are committed by the blockchain SUT in a defined time period. 

## Considerations
* Consensus Protocol Used (RAFT/Practical Byzantine Fault Tolerant)
* Geographic distribution of nodes
* Hardware environment of all peers
* Network model
* Number of nodes involved in the test transaction
* Software component dependencies
* Test tools and framework.
* Type of data store used
* Workload

## Performance Reliability Engineering (PRE) Checklist & Dashboards

### Initial Impact
* Availability
* 

## Distributed Tracing System
* Zepkin

## Reference Materials:
* https://www.hyperledger.org/wp-content/uploads/2018/10/HL_Whitepaper_Metrics_PDFVersion.pdf 
