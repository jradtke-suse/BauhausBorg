# **Kubernetes Environment Discovery Questions**

NOTE: WE/SUSE need to enter the information in this doc that we already know.

Create the “t-shirt size” concept Ajay Tomar  
---

## **1\. Environment Overview & Scope**

**Current State:**

* How many Kubernetes clusters do you currently operate?  
* What cloud provider(s) are you using? (AWS EKS, GCP GKE, Azure AKS, on-prem, hybrid?)  
* What's the total node count across all clusters? What about pod count?  
* How are your clusters organized? (by environment, team, product, region?)  
* Are you running managed Kubernetes or self-managed? What version(s)?

**Growth & Scale:**

* How has your cluster size changed over the past 6-12 months?  
* What growth rate do you anticipate over the next 12 months?  
* What's driving that growth? (more applications, more traffic, new teams?)

---

## **2\. Current Monitoring & Observability**

**Existing Tools:**

* What monitoring tools do you currently have in place?  
* Are you collecting metrics? If so, what's your retention period?  
* Do you have centralized logging? What solution?  
* How do you currently check node or pod resource utilization?  
* Do you have dashboards? Who uses them and how often?

**Visibility Gaps:**

* What questions about your environment can't you answer today?  
* When was the last time you were surprised by a capacity issue?  
* How long does it take to diagnose performance problems currently?  
* Do you have visibility into cost per application/team/namespace?

---

## **3\. Resource Management Practices**

**Current Practices:**

* What percentage of your pods have resource requests defined? Limits?  
* Do you have standards or policies for setting requests/limits?  
* How do teams determine what values to set?  
* Are you using any autoscaling? (HPA, VPA, Cluster Autoscaler?)  
* Do you have different node pools/groups for different workload types?

**Pain Points:**

* How often do you experience pod evictions or OOM kills?  
* Do you see pending pods waiting for capacity? How often?  
* Have you had incidents related to resource exhaustion?  
* Do pods frequently get scheduled on nodes that aren't optimal for them?

---

## **4\. Capacity Planning & Operations**

**Planning Process:**

* How do you currently make decisions about adding or removing nodes?  
* Who is responsible for capacity planning?  
* How far in advance do you plan for capacity needs?  
* What triggers a cluster expansion decision?  
* Have you ever had insufficient capacity for a deployment or traffic spike?

**Operational Challenges:**

* What keeps your team up at night regarding Kubernetes?  
* How much time does your team spend on capacity management weekly?  
* Do you have runbooks for scaling procedures?  
* How do you handle node maintenance or upgrades?

---

## **5\. Cost & Efficiency**

**Current Understanding:**

* Do you know how much you're spending on Kubernetes infrastructure monthly?  
* Can you break down costs by application, team, or environment?  
* Do you have budget targets or cost optimization goals?  
* Are you using spot/preemptible instances? What percentage?  
* Have you identified any "low-hanging fruit" for cost savings?

**Optimization Efforts:**

* Have you done any right-sizing exercises? What was the result?  
* Do you regularly review and adjust resource allocations?  
* Who owns cost optimization efforts?  
* What's preventing you from optimizing further?

---

## **6\. Workload Characteristics**

**Application Types:**

* What types of workloads are you running? (web apps, batch jobs, ML, databases, etc.)  
* Are your workloads stateless or stateful? What's the mix?  
* Do you have predictable traffic patterns or highly variable loads?  
* What's your peak vs. average resource utilization ratio?  
* Do you have any workloads with special requirements? (GPU, high memory, etc.)

**Performance Requirements:**

* What are your SLA/SLO targets?  
* Which applications are most critical to your business?  
* Do you have different priority classes for workloads?  
* How do you handle resource contention between applications?

---

## **7\. Team Structure & Processes**

**Organization:**

* How many teams deploy to your Kubernetes clusters?  
* Are teams self-service or is there a platform team gatekeeping?  
* What's the Kubernetes expertise level across your teams?  
* Do you have dedicated SRE/platform engineering teams?

**Workflows:**

* How do applications get deployed? (GitOps, CI/CD, manual?)  
* Who approves changes to resource requests/limits?  
* How do you communicate capacity constraints to dev teams?  
* Do you have regular review cycles for optimization?

---

## **8\. Governance & Standards**

**Policies:**

* Do you have any admission controllers or policy enforcement? (OPA, Kyverno, etc.)  
* Are there required labels, annotations, or metadata standards?  
* Do you enforce resource quotas at the namespace level?  
* How do you prevent teams from over-requesting resources?

**Compliance:**

* Are there security or compliance requirements affecting your architecture?  
* Do you need to maintain separation between certain workloads?  
* Are there data residency or multi-region requirements?

---

## **9\. Pain Points & Goals**

**Current Challenges:**

* What's the biggest challenge you face with your Kubernetes environment today?  
* If you could wave a magic wand, what would you improve?  
* What metrics or insights do you wish you had?  
* Where do you spend the most time firefighting?

**Success Criteria:**

* What would success look like for this initiative?  
* How will you measure improvement?  
* What are your top 3 priorities? (cost, performance, reliability, etc.)  
* What timeline are you working with?

---

## **10\. Technical Integration Points**

**Existing Infrastructure:**

* What other systems need to integrate with your monitoring solution?  
* Do you use infrastructure-as-code? (Terraform, CloudFormation, etc.)  
* How are your clusters deployed and managed?  
* What CI/CD tools are in your pipeline?

**Data & Reporting:**

* Who needs access to utilization data? (executives, team leads, developers?)  
* Do you need to export data to other systems? (CMDB, billing, etc.)  
* Are there existing reporting requirements or formats?  
* How do you currently communicate infrastructure metrics to stakeholders?

---

## **Prioritization Exercise**

After gathering information, I'd ask them to rank these areas:

1. **Cost reduction** \- Immediate savings through optimization  
2. **Reliability improvement** \- Prevent outages and performance issues  
3. **Operational efficiency** \- Reduce time spent on manual capacity management  
4. **Visibility & insights** \- Better understanding of what's happening  
5. **Team enablement** \- Self-service capabilities for dev teams  
6. **Future readiness** \- Scalable architecture for growth

**Final Question:** *"If we could only solve ONE problem in the next 90 days, what would have the biggest impact on your organization?"*

---

## **Follow-up Format**

Based on responses, I'd structure follow-ups as:

**Quick Wins** (0-30 days): Low-effort, high-impact improvements **Foundation Building** (30-90 days): Core infrastructure for long-term success  
**Optimization Phase** (90+ days): Continuous improvement and advanced capabilities

This approach ensures we understand not just the technical environment, but the organizational context, constraints, and success criteria that will drive a solution that actually gets adopted and delivers value.

