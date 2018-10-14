# Web Scraping Analysis of Georgia Ethics Page


1. Hit URL:   http://media.ethics.ga.gov/search/Campaign/Campaign_ByName.aspx
   ==> Displays "CAMPAIGN REPORTS - NAME SEARCH RESULTS" page
    Form with "Last name" field
    
2. Set "Last Name" = "A" (Loop through letters "A" - "Z")
    and hit "Search for Candidate" button
    ==> Displays "CAMPAIGN REPORTS - NAME SEARCH RESULTS" page
    Containing table with following columns:
        Action (fixed link "View") 
        Candidate or Committee Name
        Registration (integer)
        
3. Click on "View" link
    ==> Displays "CAMPAIGN REPORTS AND REGISTRATION INFORMATION"
    Lable: "Candidate Name:"
    Field: (Candidate name)
    
    Table:  (If candidate has run for multiple offices, they will all show up here)
        - FilerID (string, e.g. "C2017000256")
        - Office Sought (string, e.g. "Governor")
        - Candidate Information (fixed link: "Click Here To View")
        - Status (valid values: "Active", ...)
        
   Tab group:
        Tab:  "Campaign Disclosure Reports"
            Label: "Campaign Contribution Disclosure Report(s) for C2017000256:"
            
            Link 1:  "Campaign Contribution Reports - EFiled (Click to Expand Information)"
                Clicking this expands the following table:
                    - Action (Fixed link: "View Report")
                    - Type (Valid values: "Original", "Amended", ...)
                    - Year (YYYY)
                    - Report (Descriptive name, "September 30th - Election Year", "6 Days before Primary Run-Off", "June 30th - Election Year", ...)
                    - Received By ("Third Party", ...)
                    - Received (Date:  MM/DD/YYYY)
                    
                    When you click on "View Report", you get the "REPORT FORMAT OPTION" page for the candidate
                    Table containing link called "View Contributions"
                    ==> Shows "CAMPAIGN CONTRIBUTION DISCLOSURE REPORT - CONTRIBUTIONS" page
                    
                    #ctl00_ContentPlaceHolder1_Campaign_ByContributions_RFResults2_Export
                    <input type="image" name="ctl00$ContentPlaceHolder1$Campaign_ByContributions_RFResults2$Export" id="ctl00_ContentPlaceHolder1_Campaign_ByContributions_RFResults2_Export" src="../images/btnexcel.gif" style="border-width:0px;">
                    
                    
                    
            Link 2: "Two Business Day Reports (Click to Expand Information)"
                Clicking this expands the following table:
                    - Action (Fixed link: "View Report")
                    - Type (Valid values: "Original", "Amended", ...)
                    - Year (YYYY)
                    - Report (Descriptive name, "Primary Run-Off Election", ...)
                    - Received By ("E-Filing", ...)
                    - Received (Date:  MM/DD/YYYY)
                    - Status (Valid values: "Report Submitted", ...)
                    
            
        
