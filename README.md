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


# coding: utf-8

# In[1]:

import pandas as pd
import numpy as np
import datetime
import os
import sys

# In[2]:

import pytz

# In[3]:

tz_mst = pytz.timezone('America/Phoenix')


# In[4]:

def localize_datetime(df, key='date'):
    if type(df) == pd.Series:
        return df.apply(lambda x: x.tz_localize('UTC').tz_convert(tz_mst) if pd.notnull(x) else x)
    cols_date = [i for i in df.columns if key in i.lower()]
    print cols_date
    for col in cols_date:
        df[col] = pd.to_datetime(df[col])
        df[col] = df[col].apply(lambda x: x.tz_localize('UTC').tz_convert(tz_mst) if pd.notnull(x) else x)
    return df


# In[5]:

path_lead = 'geo lead.csv'
path_opp = 'geo opportunity.csv'
path_account = 'geo account.csv'
path_opp_item = 'geo opportunity_lineitem.csv'
path_opp_history = 'geo opportunity history.csv'
path_user = 'geo user.csv'

# In[6]:

out_path_lead = 'out geo lead.csv'
out_path_opp = 'out geo opportunity.csv'
out_path_account = 'out geo account.csv'
out_path_history = 'out geo history.csv'
out_path_user = 'out geo user.csv'
out_path_deal = 'out geo deal.csv'

# In[7]:

# get users
names_user = ['user_' + i for i in ['name', 'email', 'role', 'type', 'id', 'alias']]
dfuser = pd.read_csv(path_user, names=names_user, skiprows=1)
dfuser

# In[8]:

dfuser.to_csv(out_path_user, index=False)

# In[9]:

# get leads
ori_dflead = localize_datetime(pd.read_csv(path_lead))
print ori_dflead.columns
ori_dflead

# In[10]:

cols_lead = ['Id', 'CreatedDate', 'Date_for_Lead_Assignment__c',
             'LeadSource', 'Status', 'OwnerId',
             'IsConverted', 'ConvertedAccountId',
             'ConvertedOpportunityId', 'ConvertedDate',
             ]
dflead = ori_dflead[cols_lead]
dflead.columns = ['ld_' + i[:-3] if i.endswith('__c') else 'ld_' + i for i in cols_lead]

# In[11]:

dflead

# In[12]:

dflead.to_csv(out_path_lead, index=False)

# In[13]:

# get opportunity
ori_dfopp = localize_datetime(pd.read_csv(path_opp))
print ori_dfopp.columns
ori_dfopp

# In[14]:

cols_opp = ['Id', 'CreatedDate', 'StageName', 'Name', 'AccountId', 'LeadSource', 'Lead_Category__c',
            'Already_Contract_signed__c', 'Already_Closed_Won__c', 'IsWon',
            'Product_Type__c', 'Amount', 'ExpectedRevenue', 'Monthly_Commitment__c', 'OwnerId',
            'Is_subscription_started__c', 'IsClosed']
dfopp = ori_dfopp[cols_opp]
dfopp.columns = ['opp_' + i[:-3] if i.endswith('__c') else 'opp_' + i for i in cols_opp]

# In[15]:

flag_opp_test = dfopp.opp_Name.apply(lambda x: 'test' in x.lower())
print flag_opp_test.value_counts()
dfopp = dfopp[~flag_opp_test]

# In[16]:

dfopp

# In[17]:

dfopp.to_csv(out_path_opp, index=False)

# In[18]:

dfopp.opp_StageName.value_counts()

# In[19]:

dfopp[dfopp.opp_Already_Closed_Won].opp_StageName.value_counts()

# In[20]:

# IsWon: Closed
dfopp[dfopp.opp_IsWon].opp_StageName.value_counts()

# In[21]:

dfopp[dfopp.opp_IsClosed].opp_StageName.value_counts()

# In[22]:

# get account
ori_dfaccount = localize_datetime(pd.read_csv(path_account))
print ori_dfaccount.columns
ori_dfaccount

# In[23]:

cols_account = ['Id', 'CreatedDate', 'Name', 'OwnerId',
                'AccountSource', 'Account_Status__c', 'Closed_Opportunity_Lookup__c'
                ]
dfaccount = ori_dfaccount[cols_account]
dfaccount.columns = ['acc_' + i[:-3] if i.endswith('__c') else 'acc_' + i for i in cols_account]

# In[24]:

dfaccount

# In[25]:

dfaccount.loc[dfaccount.acc_AccountSource == 'EMAIL', 'acc_AccountSource'] = 'Email'

# In[26]:

dfaccount.to_csv(out_path_account, index=False)

# In[27]:

dfaccount.acc_Closed_Opportunity_Lookup.value_counts()

# In[28]:

# get opportunity history
dfhist = localize_datetime(pd.read_csv(path_opp_history))
dfhist.sort_values(['CreatedDate'], inplace=True, ascending=False)
print dfhist.columns
dfhist

# In[29]:

dfhist[['PreviousStage', 'PreviousDate']] = localize_datetime(
    dfhist.groupby('OpportunityId').shift(-1)[['StageName', 'CreatedDate']])

# In[30]:

dfhist.to_csv(out_path_history, index=False)

# In[31]:

gbhist_won = dfhist[dfhist.StageName == 'Closed Won'].groupby('OpportunityId')

# In[32]:

gbhist_won.apply(len).value_counts()

# In[33]:

dfdeal = gbhist_won.apply(lambda x: x.iloc[-1])
dfdeal.columns = ['deal_' + i[:-3] if i.endswith('__c') else 'deal_' + i for i in dfdeal.columns]

# In[ ]:




# In[34]:

dfdeal

# In[35]:

dfdeal.to_csv(out_path_deal, index=False)

# In[36]:

dfhist.StageName.value_counts()

# In[37]:

dfhist[dfhist.PreviousStage == 'Contract Signed'].StageName.value_counts()

# In[38]:

# combine


# In[39]:

flag_opp_nullsource = dfopp.opp_Lead_Category.isnull()

# In[40]:

dfopp['owner_name'] = dfuser.set_index('user_id').user_name.loc[dfopp.opp_OwnerId.values].values

# In[41]:

dfopp['opp_DealDate'] = dfdeal.loc[dfopp.opp_Id].deal_CreatedDate.values

# In[42]:

dfopp[dfopp.opp_DealDate.notnull()]

# In[43]:

dfopp['created_day'] = dfopp.opp_CreatedDate.apply(lambda x: x.date)

# In[44]:

dfopp['deal_day'] = dfopp.opp_DealDate.apply(lambda x: x.date() if pd.notnull(x) else x)

# In[45]:

dfopp = dfopp[~dfopp.opp_Lead_Category.isnull()]

# In[46]:

dfopp.opp_Monthly_Commitment, dfopp.opp_OwnerId

# In[47]:

# opps/deals by date/source


# In[48]:

dfnewdeal = dfopp.groupby(['deal_day', 'opp_Lead_Category']).apply(lambda x: pd.Series({
    'new Deals': len(x),
    'new MRR': sum(x.opp_Monthly_Commitment)
}))

# In[49]:

dfnewdeal.index.rename(['date', 'source'], inplace=True)

# In[50]:

dfnewdeal

# In[51]:

dfnewopp = dfopp.groupby(['created_day', 'opp_Lead_Category']).apply(lambda x: pd.Series({'new Opps': len(x)}))

dfnewopp.index.rename(['date', 'source'], inplace=True)

# In[52]:

dfopp.groupby(['opp_Lead_Category']).apply(lambda x: len(x))

# In[53]:

dfnewopp

# In[54]:

out_path_opp_performence_by_source = 'out geo opp performence by source.csv'

# In[55]:

dfperfm_opp_source = dfnewopp.join(dfnewdeal, how='outer').fillna(0)

# In[56]:

dfperfm_opp_source

# In[57]:

dfperfm_opp_source.to_csv(out_path_opp_performence_by_source)

# In[58]:

# opps/deals by date/owner


# In[59]:

flag_opp_downgrade = (dfopp.opp_Lead_Category == 'Downgrade')
flag_opp_downgrade.value_counts()

# In[60]:

dfopp_nodown = dfopp[~ flag_opp_downgrade]

# In[61]:

dfaedeal = dfopp_nodown.groupby(['deal_day', 'owner_name']).apply(lambda x: pd.Series({
    'new Deals': len(x),
    'new MRR': sum(x.opp_Monthly_Commitment)
}))
dfaedeal.index.rename(['date', 'owner_name'], inplace=True)

# In[62]:

dfaedeal

# In[63]:

dfaeopp = dfopp_nodown.groupby(['created_day', 'owner_name']).apply(lambda x: pd.Series({'new Opps': len(x)}))
dfaeopp.index.rename(['date', 'owner_name'], inplace=True)

# In[64]:

dfaeopp

# In[65]:

out_path_opp_performence_by_ae = 'out geo opp performence by ae.csv'

# In[66]:

dfperfm_opp_ae = dfaeopp.join(dfaedeal, how='outer').fillna(0)

# In[67]:

dfperfm_opp_ae

# In[68]:

dfperfm_opp_ae.to_csv(out_path_opp_performence_by_ae)

# In[69]:

lead_source_mapping = {

}


# In[ ]:



