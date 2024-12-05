+----------------------------------+------------------------+----------+
| ![](vertopal_                    |                        |          |
| 217a6994eab440608148f1eb536c1902 |                        |          |
| /media/image1.png){width="2.4in" |                        |          |
| height="0.5881944444444445in"}   |                        |          |
|                                  |                        |          |
| SCHOOL OF INFORMATION AND        |                        |          |
| TECHNOLOGY                       |                        |          |
+----------------------------------+------------------------+----------+
| NAME: LAURIANO, RYAN             | DATE PERFORMED:        | /40      |
|                                  | 11/19/2024             |          |
+----------------------------------+------------------------+----------+
| Section: IDC2                    | DATE SUBMITTED:        |          |
|                                  | 11/21/2024             |          |
+----------------------------------+------------------------+----------+

# SYSADM1 -- Data Loss

Instruction/s:

Read and analyze the data loss scenarios provided. Create a data
recovery plan by providing impact assessment, recovery plan and
preventive measures for each scenario. Lastly, answer the reflection
question.

**Evaluation Criteria Guide:**

1.  Impact Assessment:

-   Accurately identifies the potential consequences of the data loss.

-   Quantifies the potential financial, operational, and reputational
    impact.

    1.  Recovery Plan:

```{=html}
<!-- -->
```
-   Proposes a detailed, feasible, and timely recovery plan.

-   Includes steps for data restoration, system recovery, and business
    continuity.

-   Identifies the necessary resources and personnel.

    1.  Preventive Measures:

```{=html}
<!-- -->
```
-   Recommends specific measures to prevent similar incidents in the
    future.

-   Addresses potential vulnerabilities in security, hardware, and
    software.

-   Proposes regular backups, security audits, and employee training.

-   Recommends appropriate RAID levels for data redundancy and
    performance.

+----------------+----------------+----------------+-----------------+
| **Scenario**   | **Impact       | **Recovery     | **Preventive    |
|                | Assessment**   | Plan**         | Measures**      |
+================+================+================+=================+
| A system       | If a database  | First, I would | To prevent      |
| administrator  | with customer  | stop           | this, I would   |
| accidentally   | information    | everything to  | set up better   |
| deletes a      | gets           | avoid making   | permissions, so |
| critical       | accidentally   | it worse.      | only certain    |
| database       | deleted, it    | Then, I would  | people can      |
| containing     | could cause    | use recovery   | access critical |
| customer       | big problems.  | tools to try   | systems. I'd    |
| information    | Operations     | to get the     | also make sure  |
| while          | might stop,    | data back. If  | there are       |
| performing     | customers      | that doesn't   | regular backups |
| routine        | might get mad, | work, I would  | and train       |
| maintenance.   | and the        | check if there | everyone on how |
|                | company could  | is a backup    | to handle data  |
|                | face legal     | then try to    | safely. Having  |
|                | issues. It     | restore the    | a system that   |
|                | could also     | database from  | keeps versions  |
|                | cost a lot of  | the latest     | of the database |
|                | money to fix   | backup and     | would also      |
|                | and hurt the   | double-check   | help.           |
|                | company's      | everything is  |                 |
|                | reputation.    | correct. After |                 |
|                |                | that, I would  |                 |
|                |                | make sure      |                 |
|                |                | permissions    |                 |
|                |                | are set        |                 |
|                |                | properly so it |                 |
|                |                | doesn't happen |                 |
|                |                | again. I'd     |                 |
|                |                | also update    |                 |
|                |                | the team and   |                 |
|                |                | customers on   |                 |
|                |                | what's going   |                 |
|                |                | on.            |                 |
+----------------+----------------+----------------+-----------------+
| A major hard   | If the hard    | In this case,  | To avoid this,  |
| drive failure  | drive on a     | I would switch | I'd use RAID    |
| occurs on a    | critical       | to a backup    | for redundancy  |
| server hosting | server fails,  | server or use  | so we can       |
| essential      | it could cause | a disaster     | recover even if |
| business       | operations to  | recovery site  | a drive fails.  |
| applications,  | stop, lead to  | to keep things | I'd also check  |
| resulting in   | data loss, and | running. I'd   | the hardware    |
| data loss.     | cost a lot to  | replace the    | regularly, keep |
|                | fix. It could  | broken hard    | backups in safe |
|                | also upset     | drive and      | locations, and  |
|                | customers if   | restore data   | consider using  |
|                | services are   | from backups   | SSDs, which are |
|                | down for too   | if there is    | more reliable   |
|                | long.          | one. After     | than regular    |
|                |                | that, I'd test | hard drives.    |
|                |                | the system to  |                 |
|                |                | make sure      |                 |
|                |                | everything     |                 |
|                |                | works before   |                 |
|                |                | going live     |                 |
|                |                | again.         |                 |
+----------------+----------------+----------------+-----------------+
| A powerful     | If an          | The first step | To prepare for  |
| earthquake     | earthquake     | would be to    | disasters like  |
| strikes a data | damages a data | check what's   | this, I'd make  |
| center,        | center, it     | still usable.  | sure we have    |
| causing        | could destroy  | Then, I'd      | backups stored  |
| significant    | hardware,      | switch         | in safe         |
| damage to      | cause data     | operations to  | locations, like |
| hardware and   | loss, and shut | a cloud-based  | cloud servers   |
| power          | down           | system or a    | or data centers |
| i              | operations.    | backup data    | in other        |
| nfrastructure. | Fixing         | center while   | regions. I'd    |
|                | everything     | restoring data | also use        |
|                | could take a   | from offsite   | e               |
|                | lot of time    | backups. Once  | arthquake-proof |
|                | and money, and | things are     | equipment for   |
|                | customers      | running again, | our hardware    |
|                | might lose     | I'd focus on   | and run         |
|                | trust in the   | rebuilding or  | disaster        |
|                | company.       | replacing the  | recovery drills |
|                |                | damaged        | to be ready.    |
|                |                | systems.       |                 |
+----------------+----------------+----------------+-----------------+
| A ransomware   | A ransomware   | I would first  | To prevent      |
| attack         | attack could   | isolate the    | ransomware, I'd |
| encrypts       | lock us out of | infected       | make sure all   |
| critical data, | critical data  | system to stop | software is     |
| rendering it   | and stop       | the ransomware | updated,        |
| inaccessible.  | operations. It | from           | install         |
|                | could cost     | spreading.     | antivirus       |
|                | money to fix,  | Then, I'd      | tools, and      |
|                | and if         | report it to   | train everyone  |
|                | sensitive      | the right      | to avoid        |
|                | information is | authorities    | phishing scams. |
|                | leaked,        | and remove the | I'd also keep   |
|                | customers      | malware. After | multiple        |
|                | might lose     | that, I'd      | offline backups |
|                | trust in us.   | restore the    | that can't be   |
|                |                | data from      | affected by     |
|                |                | clean, offline | ransomware      |
|                |                | backups and    | attacks.        |
|                |                | check that the |                 |
|                |                | system is      |                 |
|                |                | secure before  |                 |
|                |                | bringing it    |                 |
|                |                | back online.   |                 |
+----------------+----------------+----------------+-----------------+
| A system       | If a backup    | I would stop   | To prevent      |
| administrator  | system is      | the backup     | this, I'd check |
| misconfigures  | misconfigured, | process to     | the backup      |
| a backup       | it could ruin  | avoid more     | system          |
| system,        | the backups,   | issues and     | regularly and   |
| leading to     | making it      | recover the    | use tools that  |
| data           | impossible to  | data from      | monitor for any |
| corruption and | restore data   | other backup   | issues. I'd     |
| loss.          | when needed.   | copies. Then,  | also keep       |
|                | This could     | I'd fix the    | multiple backup |
|                | cause long     | backup system  | copies in       |
|                | downtimes and  | and test it to | different       |
|                | upset          | make sure it   | formats, like   |
|                | customers      | works properly | on the cloud    |
|                | while costing  | before using   | and external    |
|                | money to fix.  | it again. I'd  | drives, and     |
|                |                | explain to     | train people on |
|                |                | customers and  | how to set up   |
|                |                | stakeholders   | backups         |
|                |                | what happened  | properly.       |
|                |                | and how we're  |                 |
|                |                | fixing it.     |                 |
+----------------+----------------+----------------+-----------------+
| **Reflection   |                |                |                 |
| Question**     |                |                |                 |
|                |                |                |                 |
| If some data   |                |                |                 |
| couldn't be    |                |                |                 |
| recovered then |                |                |                 |
| I would say to |                |                |                 |
| the            |                |                |                 |
| stakeholders   |                |                |                 |
| about the      |                |                |                 |
| data's that    |                |                |                 |
| can't be       |                |                |                 |
| recovered      |                |                |                 |
| either due to  |                |                |                 |
| virus or there |                |                |                 |
| is no existing |                |                |                 |
| backup for me  |                |                |                 |
| to recover the |                |                |                 |
| lost data. I   |                |                |                 |
| would explain  |                |                |                 |
| the steps that |                |                |                 |
| were taken to  |                |                |                 |
| recover the    |                |                |                 |
| data to make   |                |                |                 |
| sure that they |                |                |                 |
| will not have  |                |                |                 |
| the wrong      |                |                |                 |
| impression     |                |                |                 |
| that we are    |                |                |                 |
| not trying our |                |                |                 |
| best. Then     |                |                |                 |
| take record of |                |                |                 |
| this           |                |                |                 |
| occurrences to |                |                |                 |
| ensure that we |                |                |                 |
| can improve    |                |                |                 |
| our backup and |                |                |                 |
| recovery       |                |                |                 |
| systems so     |                |                |                 |
| that it can be |                |                |                 |
| prevented and  |                |                |                 |
| would not      |                |                |                 |
| happen again   |                |                |                 |
| in the future. |                |                |                 |
| In order to    |                |                |                 |
| mitigate the   |                |                |                 |
| impact either  |                |                |                 |
| we can check   |                |                |                 |
| for the usable |                |                |                 |
| data's and     |                |                |                 |
| implement some |                |                |                 |
| actions before |                |                |                 |
| blaming each   |                |                |                 |
| other as this  |                |                |                 |
| would lead to  |                |                |                 |
| panic.         |                |                |                 |
+----------------+----------------+----------------+-----------------+

**Grading Rubric**

  ----------------------------------------------------------------------------------
  **Criteria**   **Excellent (10       **Satisfactory (7  **Needs        **Score**
                 pts)**                pts)**             Improvement (4 
                                                          pts)**         
  -------------- --------------------- ------------------ -------------- -----------
  Impact         Accurately identifies Identifies some    Fails to       
  Assessment     all significant       key impacts but    identify       
                 impacts.              misses others.     significant    
                                                          impacts.       

  Recovery Plan  Proposes a            Proposes a basic   Fails to       
                 comprehensive,        plan but lacks     propose a      
                 detailed, and         detail or          viable plan.   
                 feasible plan.        feasibility.                      

  Preventive     Recommends strong,    Recommends some    Fails to       
  Measures       specific preventive   preventive         recommend any  
                 measures, including   measures but lacks preventive     
                 appropriate RAID      detail or          measures.      
                 levels.               specificity.                      

  Reflection     Clearly and concisely Provides a basic   Fails to       
  Question:      explains the          explanation but    provide a      
                 situation to          lacks clarity or   satisfactory   
                 stakeholders,         empathy.           explanation.   
                 acknowledging the                                       
                 limitations of data                                     
                 recovery.                                               

  **Total                                                                **/40**
  Score:**                                                               
  ----------------------------------------------------------------------------------
