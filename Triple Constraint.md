# TRIPLE CONSTRAINT

On a given project there are fundamentally three constraints:
* The amount of work you are going to deliver (Scope).
* The amount of money you are willing to spend (Budget).
* How long the project can run (Schedule)?

1. *<ins>**Scope:**</ins>* 

    Our objective is to reduce the boot time of the operating system. This is an important aspect for defining our scope for the project. This scope defines our boundary for the working programs as we are now only going to focus on the processes which are associated with our boot time and dealing with them will help us reduce boot time.

    Example: Using this command ‘systemd-analyze blame’ it will display the processes which are running at startup and we have mentioned some of them here:                                                                                                                   

    Time | Services
    -----| --------
    52.246s | dnf-makecache.service
    36.985s | plymouth-quit-wait.service                                                               
    26.665s | php-fpm.service                                                                          
    23.235s | libvirtd.service                                                                         
    21.053s | unbound-anchor.service                                                                   
    20.786s | NetworkManager-wait-online.service                                                       
    17.041s | firewalld.service                                                                        
    16.030s | httpd.service                                                                            
    13.246s | systemd-fsck@dev-mapper-fedora_localhost\x2d\x2dlive\x2dhome.service                     
    11.627s | cups.service                                                                             
    10.302s | sssd.service                                                                             
    9.956s | udisks2.service                                                                          
    9.921s | mongod.service                                                                           
    8.841s | dracut-initqueue.service                                                                 
    8.572s | lvm2-monitor.service                                                                     
    8.105s | systemd-udev-settle.service   

    This is just a snap of the processes which we are going to deal with during our scope of the project, considering each process needs development and reduction in its working we can determine the expected timespan for the project. Example: If we are dealing with 50 process then we if we spend 50-75 days considering each process days at-least 24 hours to 36 hours for development and testing of the process as a part of boot. That’s about 50 processes, and we around dealing with more than 250 processes at current for boot time for different OS.
   
2.  *<ins>**Budget**:</ins>*
    * Fixed Cost

      Human Resource:
      * consist of employees working in the project who can be project managers, project team members, Administrators etc.
      * Estimation of cost involved in paying Salaries to those employees. 
      * No. of employees in involved in project = 40
      * Average cost spent on employees per year = ₹6,00,000 

      Equipment:
      * There would be several equipment including laptops/PC's, Printers etc. would be required by the employees.
      * Estimation of Cost involved on buying/maintaining of those Equipment.
      * No. of Equipment (Laptop’s/PC's,) required for project = 100
      * Average Cost of each Equipment = ₹21,000
      * There would be some Applications required to analyze/work/testing on the project.
      * Estimation of cost required on purchasing the license of the application.
      * Average cost of Licenses for a period of a year = ₹3000 
      * There would be servers required for saving, processing, deploying work from multiple employees.
      * Cost Estimation in terms of buying, maintaining and operating the server.
      * No. of Servers Required = 1 
      * Cost per server = ₹7,00,000
      * Maintenance cost per server= ₹29,540

    * Variable Cost

      Temporary resource:
      * There would be some skilled/fresh interns required for completing some tasks in project for a specific amount of time.
      * Estimation of cost spent on payment for those interns based on months they are hired.
      * Expected No. of Skilled/Fresh Interns Expected = 20
      * Cost expected on payment to Required Interns per month = ₹20,000
      * There can be a need of external vendors who can be given contract to do certain sub project.
      * Estimation of Cost spent on Paying to those vendors.
      * Contracts based on Sub projects would require around ₹3,00,000 to ₹5,00,000 for a period of 2-3 months or time allotted by management.

      Indirect cost:
      * Electricity spent on operating various equipment inside the organization.
      * Estimation of cost spent on electricity within project deadline.
      * Expected Electricity Cost of year (as per 8 hours a day) = ₹2,80,000
      * Downtime required for the deployment of project.
      * Estimation of cost which is being lost when the system is down for particular time.
      * Expected Cost bared at the System downtime when production of project is going on 40,00,000 per hour.

3.  *<ins>**Time**:</ins>*

    The schedule of the project is determined completely based on the time required to complete the project, or produce the deliverable. This will be figured out by noting all the tasks necessary to move from start to the finish of the project. In order to attain the project goal/objective we have broken down the work into a series of more manageable tasks which can be implemented in slots and give us the required outcome, like for reducing the boot time of the operating system we may have to look into each process and then prioritize these processes depending on the requirement from the point of view of the business. After prioritizing each process, we then place it on a given timeline and work on it based on the timeline.

    Deadlines matters the most and if such is the case then there must be flexibility with the cost and the scope of the project. That would mean getting more resources, increasing cost and cutting down the scope wherein the quality of the end product wouldn't matter. For example, if we have a project to be completed within a timespan in 1year, due to certain circumstances we may have to deliver the project within 6 months this would lead to a reduction in the scope of our project and increase the cost of capital in our project. In our project, for each task to be completed a particular time slot is provided based on that each task is completed.

    In order to have our project completed it needs to be handled by making use of past project reports and predict the time span of our project to make accurate time estimates and track the progress up till date to ensure that everything is on schedule and the product is delivered on time. For example, every project has a project manager that plans the project, budget and documents all the aspects of the particular project, the project manager all takes care of the tasks that need to be completed within a particular time period and assigns tasks to the employees in that manner.
