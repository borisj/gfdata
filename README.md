# gfdata


# coding: utf-8

# In[37]:

path_lead = 'geo lead.csv'
path_opp = 'geo opportunity.csv'
path_account= 'geo account.csv'
path_opp_item= 'geo opportunity_lineitem.csv'
path_opp_history='geo opportunity history.csv'
path_user = 'geo user.csv'


# In[13]:

cols_lead = [
 'City',
 'Company',
 'ConvertedAccountId',
 'ConvertedContactId',
 'ConvertedDate',
 'ConvertedOpportunityId',
 'CreatedById',
 'CreatedDate',
 'Date_for_Lead_Assignment__c',
 'Days_to_Convert__c',
 'Email',
 'FirstName',
 'Id',
 'IsConverted',
 'IsDeleted',
 'IsUnreadByOwner',
 'LastActivityDate',
 'LastModifiedById',
 'LastModifiedDate',
 'LastName',
 'LeadSource',
 'OwnerId',
 'Phone',
 'RecordTypeId',
 'State',
 'Status',
 'UTM_Medium__c',
 'UTM_Source__c'
]


# In[21]:

query_lead = '''SELECT %s from Lead ORDER BY createddate DESC NULLS LAST''' % ','.join(cols_lead)
print query_lead


# In[18]:

cols_user = ['name', ' username', ' userrole.name', ' usertype', ' id', ' alias']


# In[19]:

query_user = '''SELECT %s FROM User''' % ','.join(cols_user)
print query_user


# In[23]:

cols_account = [
 'AccountSource',
 'Account_Status__c',
 'Closed_Opportunity_Lookup__c',
 'CreatedById',
 'CreatedDate',
 'Id',
 'Name',
 'OwnerId',
 'PrimaryContactEmail__c'
]


# In[26]:

query_account = '''SELECT %s FROM Account ORDER BY CreatedDate DESC NULLS LAST''' % ','.join(cols_account)
print query_account


# In[28]:

cols_opp = [
 'AccountId',
 'Already_Closed_Won__c',
 'Already_Contract_signed__c',
 'Amount',
 'Average_Sales_Price__c',
 'Client_Email__c',
 'CloseDate',
 'CreatedById',
 'CreatedDate',
 'ExpectedRevenue',
 'Fiscal',
 'FiscalQuarter',
 'FiscalYear',
 'ForecastCategory',
 'ForecastCategoryName',
 'HasOpportunityLineItem',
 'Id',
 'IsClosed',
 'IsDeleted',
 'IsPrivate',
 'IsWon',
 'Is_subscription_started__c',
 'LeadSource',
 'Lead_Category__c',
 'Monthly_Commitment_Fees__c',
 'Monthly_Commitment_Total__c',
 'Monthly_Commitment__c',
 'Name',
 'NextStep',
 'Num_of_Agreements__c',
 'OneTimeFees__c',
 'One_Time_Fees__c',
 'OwnerId',
 'Previous_Opportunity__c',
 'Probability',
 'Product_Type__c',
 'Renewal__c',
 'Setup_Fees__c',
 'StageName',
 'TotalOpportunityQuantity',
 'Total_Amount__c'
]


# In[30]:

query_opportunity = '''SELECT %s FROM Opportunity ORDER BY CreatedDate DESC NULLS LAST''' % ','.join(cols_opp)
print query_opportunity


# In[33]:

cols_opp_history = [
 'Amount',
 'CloseDate',
 'CreatedById',
 'CreatedDate',
 'ExpectedRevenue',
 'ForecastCategory',
 'Id',
 'IsDeleted',
 'OpportunityId',
 'Probability',
 'StageName',
 'SystemModstamp']


# In[36]:

query_opportunity_history = '''SELECT %s FROM OpportunityHistory ORDER BY CloseDate DESC NULLS LAST'''% ','.join(cols_opp_history)
print query_opportunity_history




# coding: utf-8

# In[37]:

path_lead = 'geo lead.csv'
path_opp = 'geo opportunity.csv'
path_account= 'geo account.csv'
path_opp_item= 'geo opportunity_lineitem.csv'
path_opp_history='geo opportunity history.csv'
path_user = 'geo user.csv'


# In[13]:

cols_lead = [
 'City',
 'Company',
 'ConvertedAccountId',
 'ConvertedContactId',
 'ConvertedDate',
 'ConvertedOpportunityId',
 'CreatedById',
 'CreatedDate',
 'Date_for_Lead_Assignment__c',
 'Days_to_Convert__c',
 'Email',
 'FirstName',
 'Id',
 'IsConverted',
 'IsDeleted',
 'IsUnreadByOwner',
 'LastActivityDate',
 'LastModifiedById',
 'LastModifiedDate',
 'LastName',
 'LeadSource',
 'OwnerId',
 'Phone',
 'RecordTypeId',
 'State',
 'Status',
 'UTM_Medium__c',
 'UTM_Source__c'
]


# In[21]:

query_lead = '''SELECT %s from Lead ORDER BY createddate DESC NULLS LAST''' % ','.join(cols_lead)
print query_lead


# In[18]:

cols_user = ['name', ' username', ' userrole.name', ' usertype', ' id', ' alias']


# In[19]:

query_user = '''SELECT %s FROM User''' % ','.join(cols_user)
print query_user


# In[23]:

cols_account = [
 'AccountSource',
 'Account_Status__c',
 'Closed_Opportunity_Lookup__c',
 'CreatedById',
 'CreatedDate',
 'Id',
 'Name',
 'OwnerId',
 'PrimaryContactEmail__c'
]


# In[26]:

query_account = '''SELECT %s FROM Account ORDER BY CreatedDate DESC NULLS LAST''' % ','.join(cols_account)
print query_account


# In[28]:

cols_opp = [
 'AccountId',
 'Already_Closed_Won__c',
 'Already_Contract_signed__c',
 'Amount',
 'Average_Sales_Price__c',
 'Client_Email__c',
 'CloseDate',
 'CreatedById',
 'CreatedDate',
 'ExpectedRevenue',
 'Fiscal',
 'FiscalQuarter',
 'FiscalYear',
 'ForecastCategory',
 'ForecastCategoryName',
 'HasOpportunityLineItem',
 'Id',
 'IsClosed',
 'IsDeleted',
 'IsPrivate',
 'IsWon',
 'Is_subscription_started__c',
 'LeadSource',
 'Lead_Category__c',
 'Monthly_Commitment_Fees__c',
 'Monthly_Commitment_Total__c',
 'Monthly_Commitment__c',
 'Name',
 'NextStep',
 'Num_of_Agreements__c',
 'OneTimeFees__c',
 'One_Time_Fees__c',
 'OwnerId',
 'Previous_Opportunity__c',
 'Probability',
 'Product_Type__c',
 'Renewal__c',
 'Setup_Fees__c',
 'StageName',
 'TotalOpportunityQuantity',
 'Total_Amount__c'
]


# In[30]:

query_opportunity = '''SELECT %s FROM Opportunity ORDER BY CreatedDate DESC NULLS LAST''' % ','.join(cols_opp)
print query_opportunity


# In[33]:

cols_opp_history = [
 'Amount',
 'CloseDate',
 'CreatedById',
 'CreatedDate',
 'ExpectedRevenue',
 'ForecastCategory',
 'Id',
 'IsDeleted',
 'OpportunityId',
 'Probability',
 'StageName',
 'SystemModstamp']


# In[36]:

query_opportunity_history = '''SELECT %s FROM OpportunityHistory ORDER BY CloseDate DESC NULLS LAST'''% ','.join(cols_opp_history)
print query_opportunity_history


