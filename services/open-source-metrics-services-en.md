# Metrics Service

## Introduction


The health metrics of an open source project are quantitative and qualitative benchmarks that assess its sustainability, community engagement, code quality, and ecosystem impact, providing critical insights for maintainers, contributors, and stakeholders.These metrics are highly valuable for assessing a project's current status, forecasting its development trending, and identifying potential risks in advance.


## 1. Popular Evaluation Frameworks for Open Source Project Health

### 1.1 CHAOSS Metrics System

CHAOSS is a project under the Linux Foundation that focuses on defining community health through metric-based analysis. The CHAOSS project has the following four objectives:

（1）Develop standardized metrics and models to evaluate the health of open source communities.

（2）Develop open source tools and initiatives for measuring community health.

（3）Formulate a plan to implement indicators that cannot be achieved through data tracking.

（4）Collaborate with global partners to redefine how open source community health is measured

### 1.2 Evolution of development stages 
##### Early stage (5 working group models)

 
| working group name | core secters|
|-----------|-------------|
| General Metrics Working Group (Current Metrics Development Working Group | Contribution types, contributors, contribution locations, time dimension|
| Diversity, Equity, and Inclusion Working Group | Communication inclusiveness, contributor diversity, activity diversity, governance structure |
| Progress Working Group| Code development activity/efficiency/quality, issue resolution, community growth|
| Value Working Group (inactive) | Measuring the value of open source participation|
| Risk Management Working Group | Business risk, code quality, licensing, security, transparency, and dependency risk|

#####  Latest Developments
- **Ungrouped indicator list**：The 89 indicators are shown in a single list without any categorization.
- **Model-driven Transformation**：

  -  Huawei company initiated the establishment of the Metrics Evaluation Model Working Group.

  - In 2023, the CHAOSS community shifted its focus toward the Working Group on Evaluation Models.

  - Up to 2025, a total of 17 metrics models have been released by CHAOSS.

### 1.3 Typical Model Example: Development Responsiveness
**Definition**：A comprehensive evaluation model reflecting a project's operational capability.
Responsiveness can reflect the level of investment in a project (including abandonment), capabilities, and engineering priorities.
It may also reflect certain types of interactions and contributors.Responsiveness can reveal a lot — including things you might overlook — such as how effective bots are at addressing Challenges

**indicators**：
1. **Change Request Review Cycle**
   - Measures the time taken for the complete review process
   - Identifies bottlenecks in the review workflow

2. **Change Request Duration**
   - Only accepted change requests are counted
   - Reflects overall processing efficiency

3. **Issue Response Time**
   - Time to First Non-Author Response
   - Measure the responsiveness of the community

4. **Bug Resolution Duration**
   - Median Duration from Issue Reporting to Resolution
   - Reflects the efficiency of the maintenance team

### 1.4 System Evaluation
##### Advantages
- Open Governance Model for Global Collaboration
- Providing rich insights into metrics design
- Demonstrating continuous evolution from discrete metrics to evaluation models

##### Chanllenges
-  Overlapping and redundant metrics (e.g., Evolution group and Risk group)
-  Excessive granularity limits practical applicability
-  Decreasing adoption in community implementations

##### Lessons Learned
- A balance is needed between metric completeness and practicality
- Model-driven approaches are an important direction for future development
- More real-world case validation is required



### 2.Health Checklist From Red Hat

In March 2021, Red Hat released a checklist for measuring the health of open source projects.In contrast to CHAOSS, the checklist introduces a clear and streamlined framework, dividing the evaluation of open source project health into seven primary categories and over ten subcategories. The checklist for evaluating the health of open source projects is as follows:

#### 1.Infrastructures  
-  Project website
-  Governance Document


#### 2.Licensing Agreement 
- Open Source License

#### 3. Leadership and Governance
-  Governance Model
-  Decision-Making Process

#### 4.Release Management
|  Subcategory   | Checklist Item             |
|------------|---------------------|
| Release Frequency   | Regular/Irregular |
| Release Conventions | Conventions for version numbering, etc.   |
| Release tools  | Release Toolchain in Use    |
| Release Availability | Availability of Installation Packages   |

#### 5. Newcomer Training
- Newcomer Guideline   
- Contributor Development Program

#### 6. Document system
- Content and Style Standards
- Documentation Writing Guidelines

#### 7. Operation
- Project Information Release
- Promotion Activity Frequency
- Community Contribution Guidance

#### Evaluation and Analysis of Red Hat's Checklist
Although it helps to quickly understand the concepts and scope related to open source project health, it offers limited practical guidance for further implementation.













### 3. OSS Compass: The Open Source Compass
Launched in 2023, OSS is China's first open source ecosystem health assessment platform. OSS Compass was jointly developed by leading domestic universities, enterprises, and open source communities. It is a platform that combines theoretical depth with practical value.The Open Source Compass showcases an open source ecosystem evaluation system that includes the open source ecosystem, "collaboration, people, software", and an evaluation model.

![图1 OSS Compass 开源指南针的开源生态评估体系](https://github.com/December21-dev/osewp/blob/main/images/open-source-ecosystem-evaluation-framewor-english.jpg)

*Figure 1. The open source ecosystem evaluation system of OSS Compass*

 For the open source ecosystem, **OSS Compass**  have established a model comprising three core dimensions: productivity, robustness, and Creativity.
#### 3.1 Productivity：The capability of transforming inputs into outputs in open source ecosystem.
(1) Collaborative Index

|  Indicator              |    Definition                                                                                 | Threshold    | Weight    |
|------------------------|------------------------------------------------------------------------------------------|--------|---------|
| Number of code contributors        | Number of active code committers, code reviewers, and PR submitters in the past 90 days | 1000   | 19.99%  |
|  Code Commit Frequency  |  Average Weekly Code Commits(Past 90 Days)                                                          | 1000   | 16.36%  |
|  Maintenance Activity     | Single-repo metric: Weekly commit occurrence (90-day period)；Multi-repo metric: Active Repository Percentage(30-Day Period)  | 100%   | 13.85%  |
|  PR-linked Commit Ratio  |  Percentage of Code Commits Linked to PRs(Past 90 Days)                                                       | 100%   | 12.61%  |
|  PR-to-Issue Linkage Ratio     |  Percentage of New PRs Linked to Issues(Past 90 Days)                                                      | 100%   | 11.32%  |
| Code Review Rate           | Percentage of Code Commits with Non-Author Reviews(Past 90 Days)                                 | 100%   | 10.11%  |
| Code Merge Ratio          |  Percentage of Non-Author Merge(Past 90 Days)                                         | 100%   | 10.11%  |
|  Lines of Code (LOC)              | Avg. Weekly LOC Changed(Past 90 Days)                                            | 300000 | 5.64%   |

(2) Community Services and Support Index

| Indicator              | Definition                                                                                     | Threshold   | Weight   |
|------------------------|------------------------------------------------------------------------------------------|--------|---------|
| Number of Updated Issues          | Number of Issues Updated（Past 90 days）                        | 2000   | 19.72%  |
| Number of Closed Pull Requests          |  Number of merged and closed PRs（Past 90 days）                | 4500   | 19.72%  |
| Time to First Issue Response     |Mean and median time to first response for new issues (in days), excluding bot replies, creator comments, and assignment actions         | 15     | -14.37%  |
| Time to Resolve Bug Issues   |Avg. & Median Bug Issue Resolution Time(incl. closed & unresolved, days)                         | 60     | -12.88%  |
|Time to Resolve PRs           |Avg. & Median PR Resolution Time(incl. merged & unmerged, days)                              | 30     | -12.88%  |
| Issue Comment Frequency          | Avg. Comments per New Issue(excl. bot & author)                                           | 5      | 10.22%  |
|  Code Review Comment Frequency       | Average Comments per New PR (excluding bots and author comments)           | 8      | 10.22%  |

#### 3.2 Robustness：Ecosystem Resilience

（1） Active participation：

|  Indicator              | Definition                                                                                     | Threshold  | Weight   |
|------------------------|------------------------------------------------------------------------------------------|--------|---------|
| Number of Contributors             | Number of active code committers, PR authors, reviewers, issue authors, and commenters （Past 90 days）                      | 2000   | 18.01%  |
| Code Commit Frequency           |  Avg. Weekly Commits(Past 90 Days)                                                          | 1000   | 18.01%  |
| Last Updated              |Avg. Time Since Last Repo Update(months)                                                   | 0.25   | 12.74%  |
|  Number of Organizations              | Active Committer Organizations(Past 90 Days)                                                 | 10     | 11.50%  |
| Created On                 | Time Since Repository Creation(months)                                                      | 120    | 7.77%   |
| Issue Comment Frequency          |  Avg. Comments per New Issue(excl. bot & author                                            | 5      | 7.77%   |
| Code Review Comment Frequency       | Avg. Comments per New PR (excl. bot & author)                                      | 8      | 4.92%   |
| Number of Issues Updated          |    Number of Issue Updates（Past 90 Days）                | 2500   | 4.92%   |
|Number of Recent Releases       | Number of Releases    （Past 90 Days)            | 12     | 3.18%   |
| Number of Maintainers             | Number of Active Maintainers（Past 90 Days)                  | 100    | 2.09%   |
|   Number of Meetings         | Number of Meetings Held（Past 90 Days)                   | 100    | 2.09%   |
|  	Number of Participants         |  Average Number of Participants per Meeting(Past 90 Days)                                                      | 10     | 2.09%   |

#### 3.3 Creativity：Capacity for Diverse Innovation
（1） Organization Activity Indicator

| Indicator              | Definition                                                                                   | Threshold   | Weight    |
|------------------------|------------------------------------------------------------------------------------------|--------|---------|
|  Number of  Organizations              | Number of Organizations Affiliated with Active Code Contributors(Past 90 Days)                 | 30     | 32.26%  |
| Number of Organizational Contributors         | Number of Active Code Contributors with Organizational Affiliation (Past 90 Days)      | 300    | 25.81%  |
| Organizational Code Submission Frequency  | Average Weekly Code Commits by Organization-Affiliated Contributors (Past 90 Days)                    | 800    | 25.81%  |
|Sustained Organizational Contribution          | Cumulative Number of Weeks with Code Contributions by All Organizations (Past 90 Days)              | 200    | 16.13%  |

#### 3.4 Productivity Supplementary Model
1. **Contributor Domain Classification Model**：
   - observation, issue, code contribution, forum discussions, media engagement, event participation, sponsorship.
2. **Contributor Role Classification Model**：
   - organizational/Individual Maintainers,Organizational/Individual Contributors
3. **Contributor Journey Model**：
   - Core, Regular, Occasional, Silent, and Stateless.

#### 3.5 The Evaluation of OSS Compass Framework 
   - Clear Top-Level Architecture Design
   - Executable Layered Metrics Breakdown
   - Observable Quantitative Measurements
2. **Practical Value**：
   - Offers the open-source compass platform
   - Supports direct use on official site or local deployment
   - Ensures high usability and operability
