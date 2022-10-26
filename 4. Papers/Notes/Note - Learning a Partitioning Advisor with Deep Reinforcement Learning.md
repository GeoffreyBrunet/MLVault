**MOC**:: [[4. Papers MOC]]
**Link**: https://arxiv.org/abs/1904.01279
**Notes**: [[PDF - Learning a Partitioning Advisor with Deep Reinforcement Learning]]
**Tags**:: #paper 
## Abstract
```
Commercial data analytics products such as Microsoft Azure SQL Data Warehouse or Amazon Redshift provide ready-to- use scale-out database solutions for OLAP-style workloads in the cloud. While the provisioning of a database cluster is usually fully automated by cloud providers, customers typ- ically still have to make important design decisions which were traditionally made by the database administrator such as selecting the partitioning schemes.

In this paper we introduce a learned partitioning advisor for analytical OLAP-style workloads based on Deep Reinforce- ment Learning (DRL). The main idea is that a DRL agent learns its decisions based on experience by monitoring the rewards for different workloads and partitioning schemes. We evaluate our learned partitioning advisor in an exper- imental evaluation with different databases schemata and workloads of varying complexity. In the evaluation, we show that our advisor is not only able to find partitionings that outperform existing approaches for automated partitioning

design but that it also can easily adjust to different deploy- ments. This is especially important in cloud setups where customers can easily migrate their cluster to a new set of (virtual) machines.
```
