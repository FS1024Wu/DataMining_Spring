[DataScience_Report.pdf](https://github.com/FS1024Wu/DataScience_Spring/files/3379744/DataScience_Report.pdf)
* follow the step, you would be able to execute and see the result.
* prerequiment:  python IDLE 64 BITS. dependency python: glob, Pillow, xlrd, numpy, pandas make sure you have all of them
* need complete dataset? contact info: fangshion@gmail.com Sheng Wu
* linear regression and logistic regreesion used, there are many algos you can use RBM, NN, DNN, I have my RBM and DNN coming soon.
*stay tuned.

1. unzip it to your local machine

2. open DS_FP_LinReg.py and DS_FP_LogReg.py change to your dictory 
such as: This is training dirctory
 tData = pd.read_excel(r"C:\Users\sheng\Desktop\DataMining\finalProj\train.xlsx", sheet_name='Sheet1')
    print("Column headings:", tData.columns)
    for filename in glob.glob(r"C:\Users\sheng\Desktop\DataMining\finalProj\*.JPG"):

edit it to your path: 
 tData = pd.read_excel(r"YOURPATH\train.xlsx", sheet_name='Sheet1')
    print("Column headings:", tData.columns)
    for filename in glob.glob(r"YOURPATH\*.JPG"):


such as: This is testing dirctory
 test_Data = pd.read_excel(r"YOURPATH\train.xlsx", sheet_name='test')
    for filename in glob.glob(r"YOURPATH\test\t1.*"):
Step 2 applys to both Lin_Reg and Log_Reg python file

3. then run your code. minimum machine requires 2 Ghz processor with 12 G RAM.
	however, you can at line 26 and 70 edit it as: 
im=Image.open(filename).resize((56,56)).convert('RGBA')#resize to smallest due memroy and matrix issue bestfit 64,64
to 
im=Image.open(filename).resize((28,28)).convert('RGB')#resize to smallest due memroy and matrix issue bestfit 64,64
even 14,14 if you like. 

4. if somehow you get singular matrix error, add bias rand.random(0,1) in line 54 & 57 just to make element in matrix nonzeor.
5. logistic regression part you might encouter the situation that you cant meet the convergence of gradient descent or ascent, you just
   need to increase the number of iteration from 2000 to 5000 or more, feel exhusted？increase the learnig rate some fration very little.
   still too slow? increase the precision from 0.0001 to 0.0005.  logistic is tend to have slow trainning time, but the accuracy very
   decent. The key is to understand the gradient decent or ascent in data science, and weight, bias as well.
 
![ct1](https://user-images.githubusercontent.com/46949426/59968850-c2b17000-950e-11e9-8fdc-d3e58d2fbf1d.png)
![ct2](https://user-images.githubusercontent.com/46949426/59968873-60a53a80-950f-11e9-8875-c961d5cee281.png)
![ct3](https://user-images.githubusercontent.com/46949426/59968941-736c3f00-9510-11e9-9f08-9261e406a02f.png)
