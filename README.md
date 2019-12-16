# PORTAL-CAPITOLE

<p align="center">
    <img src="./media/capitole-logo.png" alt="preview" />
</p>

## PREREQUISITES :construction:
Having **node** and **npm** installed.
https://www.npmjs.com/get-npm

## INSTALL :construction:

```
npm install
npm install -g newman
```

## USAGE :wrench:
### Check in/out:
Run the following command with, replacing the arguments with your personal information:
```
newman run check_in_out.json --global-var username=[EMAIL] --global-var password=[PASSWORD]--global-var action=[IN/OUT]
```

NEW!!  

Now you can specify your custom location with the following parameters. If not, it will get the default ones:  
Latitude: 41.3907285  
Longitude: 2.1745088999999997  

```
--global-var latitude=[LATITUDE] --global-var longitude=[LONGITUDE]
```

The script will detect automatically if it's a working day in your calendar, and if yes, it will perform the check-in/out action.
### Timesheet:
Run the following command with, replacing the arguments with your personal information:
```
newman run timesheet.json --global-var username=[EMAIL] --global-var password=[PASSWORD] --global-var startDate=[DD/MM/YYYY] --global-var endDate=[DD/MM/YYYY] --global-var hours=[HOURS] --global-var week=[ALL/EXCEPT-FRIDAYS/FRIDAYS]
```

Where "week" variable could be:  
**ALL** = M,T,W,TH,F  
**EXCEPT-FRIDAYS** = M,T,W,TH  
**FRIDAYS** = F  

Example:  
```
newman run timesheet.json --global-var username=foo@bar.com --global-var password=123456 --global-var startDate=01/01/2019 --global-var endDate=31/01/2019 --global-var hours=8.5 --global-var week=EXCEPT-FRIDAYS
```
```
newman run timesheet.json --global-var username=foo@bar.com --global-var password=123456 --global-var startDate=01/01/2019 --global-var endDate=31/01/2019 --global-var hours=6 --global-var week=FRIDAYS
```

## AUTHOR 
Antonio REYES (https://github.com/antreyes)
