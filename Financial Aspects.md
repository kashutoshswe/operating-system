# FINANCIAL ASPECTS

## Net Present Value (NPV)

Net present value (NPV) is the difference between the present value of cash inflows and the present value of cash outflows over a period of time. NPV is used in capital budgeting and investment planning to analyze the profitability of a projected investment or project.

**Formula for calculating NPV:**
```
NPV (i, n) = ∑_(i=0)^n  R_t/〖(1+i)〗^t 
```
Where; 
  
      n = total number of periods
      t = time of the cash flow
      i = discount rate (the rate of return that could be earned on an investment) 
      Rt = net cash flow i.e. cash inflow - cash outflow at time t (R: it is subtracted from the whole as any initial investment during 1st year is not discounted for NPV purpose).

Our company is going to launch a new product with the aspect of operating system. The new product will have startup costs, operational costs, and incoming cash flows over 5 years. This project will have an immediate (t = 0) cash outflow of ₹7,60,000 (which might include machinery, 5% taxes and employee training costs). Other cash outflows for years 1-5 are included above. Cash inflows for 1-5 years are given below in the calculations. All cash flows are after tax and there are no cash flows expected after year 5. The required rate of return is 20%. The present value (PV) can be calculated for each year.

Assuming the following for the calculation of the NPV:
Startup cost = ₹30,00,000
Operational cost = ₹8,00,000
Cash outflow [Machines, Employees, Training cost & 5% taxes]:
20% of Investment which is = ₹7,60,000
cash inflow = Income of 5 years 
Discount = 5 %

Year | Cash Flow | Present Value
---- | --------- | -------------
0	| (₹-38,00,000)/1	| ₹-38,00,000
1	| (₹10,00,000 - ₹7,60,000)/1.05	| ₹2,28,570
2	| (₹15,50,000 - ₹7,60,000)/1.1025	| ₹7,16,553
3	| (₹20,00,000 - ₹7,60,000)/1.157	| ₹10,72,000
4	| (₹20,00,000 - ₹7,60,000)/1.214	| ₹10,22,000
5	| (₹25,00,000 - ₹7,60,000)/1.275	| ₹13,65,000

* *Year 0*
  * Investment = ₹-38,00,000

* *Year 1*
  * Cash inflow = ₹10,00,000
  * Cash outflow = ₹7,60,000
	  
* *Year 2*
  * Cash inflow = ₹15,50,000
  * Cash outflow = ₹7,60,000
	  
* *Year 3 *
  * Cash inflow = ₹20,00,000
  * Cash outflow = ₹7,60,000
	  
* *Year 4 *
  * Cash inflow = ₹20,00,000
  * Cash outflow = ₹7,60,000
	  
* *Year 5*
  * Cash inflow = ₹25,00,000
  * Cash outflow = ₹7,60,000
  
```  
NPV = Aggregate of present value of 5 years - Investment
    = ₹44,04,150 - ₹38,00,000
    = ₹6,04,150
```

![NPV Line Graph](https://github.com/Ashutoshcoder/operating-system/blob/master/images/NPV_graph1.PNG)

The NPV Decision Rules |
---------------------- |
If NPV > 0, accept the project |
If NPV = 0, accept or reject the project |
If NPV < 0, reject the project |

![NPV Graph](https://github.com/Ashutoshcoder/operating-system/blob/master/images/NPV_graph2.PNG)

Conclusion: After calculating the NPV for the past 5 years, we got ₹6,04,150 as the Net Profit Value. Therefore, we should accept the project as per the NPV decision rules.

## Internal Rate of Return (IRR)

Internal rate of return (IRR) is the interest rate at which the net present value of all the cash flows (both positive and negative) from a project or investment equal zero. Internal rate of return is used to evaluate the attractiveness of a project or investment.

**Formula for calculating IRR:**
```
IRR = ((Cash flow))/〖(1+r)〗^i  – Initial Investment
```
Where; 
  
     cash flows = cash flows in the time period
     r = discount rate
     i = time period

***
**Case: 1**

A Company ABC ltd. must decide whether to accept a project of Operating System development or not. The project would initially cost Rs. 30,00,000 for the development. As per the considered objectives, project would take 4 years to be completely launched in the market, but it is expected to generate the additional profit of Rs. 6,00,000 during those years as small modules of the project will be launched every year. The project should return about 20%.

Assumptions:
Capital investment = 30,00,000
Cash flow for 3 years = 6,00,000 (per year)

Year | Cash Flow | Rate of Return
---- | --------- | --------------
1	| ₹6,00,000/(1+0.20)^1 	| ₹5,00,000
2	| ₹6,00,000/(1+0.20)^2 	| ₹4,16,666.67
3	| ₹6,00,000/(1+0.20)^3 	| ₹3,47,222.23

0 is greater than -17,36,111 (-30,00,000 + 5,00,000 + 4,16,666.67 + 3,47,222.23).
As the assumed rate of return, i.e., 20% gives the calculation result smaller than 0(zero), which means in the long run our project will not give a higher rate of return, hence, **Project is Rejected.**

***
**Case: 2**

A Company ABC ltd. must decide whether to accept a project of Operating System development or not. The project would initially cost Rs. 30,00,000 for the development. As per the considered objectives, project would take 4 years to be completely launched in the market, but it is expected to generate the additional profit of Rs. 6,00,000 during those years as small modules of the project will be launched every year. The project should return about 10%.

Year | Cash Flow | Rate of Return
---- | --------- | --------------
1	| ₹6,00,000/(1+1.24)^1 	| ₹ 483870.967
2	| ₹6,00,000/(1+1.24)^2 	| ₹ 390218.522
3	| ₹6,00,000/(1+1.24)^3 	| ₹ 314795.383
4	| ₹6,00,000/(1+1.24)^4 	| ₹ 253807.106

The investment's IRR is 24%, which is the rate that makes the present value of the investment's cash flows greater than or equal to zero. From a purely financial standpoint, Company ABC should move ahead with the project since this generates a 24% return for the Company which is much higher than the assumed 10% rate of return.

IRR is found on the basis of mathematical trial and error so that the appropriate rate can be derived in order to get the present value of cash flows greater or equal to zero, to **accept the project.**

***
