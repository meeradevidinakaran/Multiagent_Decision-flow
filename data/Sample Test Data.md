# Product Feature Launch 
We are considering launching an AI-powered product recommendation engine on 
NovaCart's checkout page. The feature uses collaborative filtering to suggest add-on items, 
targeting a 12% increase in Average Order Value (AOV). The rollout plan is a 10% traffic 
canary with a kill switch. Current p95 latency is 320ms against an SRE bar of 400ms. 
Privacy review has not been completed — the model uses browsing history and purchase 
data. Stakeholders include the VP of Product, SRE Lead, and Privacy/Legal. The main 
options are: (A) Launch to 10% immediately with monitoring, (B) Delay 2 weeks for privacy 
review and load testing, or (C) Launch a stripped-down version without personalized data. 
Success metrics are AOV lift, conversion rate, and latency impact. The decision is needed 
by end of sprint (2 weeks). Budget for the feature is already allocated. 
# Platform Migration Decision 
NovaCart's engineering team is evaluating migrating the core e-commerce platform from a 
monolithic architecture to microservices. Current deployment cycles take 3 weeks; the target 
is 3 days. Estimated migration cost is $1.2M over 12 months with a team of 8 engineers. 
Revenue risk during migration is estimated at 2-5% due to potential downtime. Options: (A) 
Full migration over 12 months, (B) Strangler pattern — migrate incrementally over 18 
months, (C) Stay on monolith and optimize CI/CD only. Key constraints: Black Friday freeze 
in November, 99.95% uptime SLA, and the current monolith serves 4M daily active users. No 
load testing has been done for the microservices prototype. The CTO, VP Engineering, and 
CFO are stakeholders. 
# Vendor Selection 
NovaCart needs to select a cloud data warehouse for its analytics platform. Current Redshift 
cluster costs $18K/month and query performance degrades during peak hours. Options: (A) 
Migrate to Snowflake ($22K/month estimated, better concurrency), (B) Migrate to BigQuery 
(pay-per-query, estimated $15K-25K/month), (C) Optimize existing Redshift with RA3 nodes 
($20K/month). Data volume is 14TB growing 2TB/quarter. 12 analysts and 3 data engineers 
are daily users. Migration timeline constraint: must complete before Q4 planning cycle. No 
POC has been run on Snowflake or BigQuery. Security review for cross-cloud data transfer 
is pending. 
