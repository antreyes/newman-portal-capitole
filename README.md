# portal-capitole

<p align="center">
    <img src="./media/capitole-logo.png" alt="preview" />
</p>

## Prerequisites :construction:
Having **node** and **npm** installed.
https://www.npmjs.com/get-npm

## Install :construction:

```
npm install
npm install -g newman
```

## Usage :wrench:
### Check IN/OUT:
Run the following command with, replacing the arguments with your personal information:
```
newman run check_in_out.json --global-var username=[EMAIL] --global-var password=[PASSWORD]--global-var action=[IN/OUT]
```
The script will detect automatically if it's a working day in your calendar, and if yes, it will perform the check-in/out action.
### Timesheet
Run the following command with, replacing the arguments with your personal information:
```
newman run timesheet.json --global-var username=[EMAIL] --global-var password=[PASSWORD] --global-var startDate=[DD/MM/YYYY] --global-var endDate=[DD/MM/YYYY] --global-var hours=[HOURS] --global-var week=[ALL/EXCEPT-FRIDAYS/FRIDAYS]
```

Where "week" variable could be:  
**ALL** = M,T,W,TH,F  
**EXCEPT-FRIDAYS** = M,T,W,TH  
**FRIDAYS** = F  

## Author 
Antonio REYES (https://github.com/antreyes)
