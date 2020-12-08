# Project Three Business Intelligence #

## Can we create an entire data pipeline from Data procurement to Business Intelligence Tool use? And do it for free? ##

### Here is our basic Architecture: ###



[.](<a href="https://imgur.com/pVhZWpd"><img src="https://i.imgur.com/pVhZWpd.jpg" title="source: imgur.com" /></a>)

### So lets get our Data into the AWS ethosephere ###

[.](<a href="https://imgur.com/yYH5KZ5"><img src="https://i.imgur.com/yYH5KZ5.jpg" title="source: imgur.com" /></a>)
[.](<a href="https://imgur.com/UKxPRS2"><img src="https://i.imgur.com/UKxPRS2.jpg" title="source: imgur.com" /></a>)

### Detailed Instructions for this step can be found [here](https://docs.aws.amazon.com/redshift/latest/gsg/getting-started.html) ###

## Now we need to create our table in our redshift server to query ##

```SQL
CREATE TABLE mytable(
   Uniq_Id               VARCHAR(MAX) NOT NULL distkey sortkey 
  ,Product_Name          VARCHAR(MAX) 
  ,Brand_Name            VARCHAR(MAX)
  ,Asin                  VARCHAR(MAX)
  ,Category              VARCHAR(MAX)
  ,Upc_Ean_Code          VARCHAR(MAX)
  ,List_Price            VARCHAR(MAX) 
  ,Selling_Price         VARCHAR(MAX)
ETC ETC ETC

copy mytable from 's3://project-three-business-intelligence/marketing_sample_for_amazon_data.csv'
credentials 'aws_iam_role=arn:aws:iam::ENTERYOUROWNINFO'
ignoreheader 1
delimiter ',' region 'us-east-2'
removequotes
emptyasnull
blanksasnull
maxerror 5;

```

[.]()

## Now that we have a table setup in our redshift lets use a jupyter notebook and read from it ##

```python
dbname = 'dev'
host = 'project-three-bi.{endpoint_data}.us-east-2.redshift.amazonaws.com'
user = 'username'
password = 'password'
port = '5439'

endpoint = f"postgresql://{user}:{password}@{host}:{port}/{dbname}"

my_connection = create_engine(endpoint)
query = "SELECT * FROM mytable;"
df = pd.read_sql(query, my_connection)
df.head()
```
[.](<a href="https://imgur.com/OnszAmE"><img src="https://i.imgur.com/OnszAmE.jpg" title="source: imgur.com" /></a>)
### looks like we are up and running ###


## What if we would like to look at How many of each category we have availbale? ##

```python
df['parent_category'] = df['category'].apply(lambda row: row.split('|')[0])
df[['category', 'parent_category']].head()

top_ten_category = pd.DataFrame(df['parent_category'].value_counts()[:10])
cols = ['category', 'count']
top_ten_category_df = top_ten_category.reset_index()
top_ten_category_df.columns = cols
top_ten_category_df

```
### The above code splits out the first position category grouping as it is the most general we can use, further cetgory names will be too specific. ###
### This is what we get out of that ###
[.](<a href="https://imgur.com/p7i8oX3"><img src="https://i.imgur.com/p7i8oX3.jpg" title="source: imgur.com" /></a>)

## ENTER TITLE HERE ##

```python
s = "Python syntax highlighting"
print s
```

[.]()

## ENTER TITLE HERE ##

```python
s = "Python syntax highlighting"
print s
```

[.]()

## ENTER TITLE HERE ##

```python
s = "Python syntax highlighting"
print s
```

[.]()

## ENTER TITLE HERE ##

```python
s = "Python syntax highlighting"
print s
```

[.]()

## ENTER TITLE HERE ##

```python
s = "Python syntax highlighting"
print s
```

[.]()
