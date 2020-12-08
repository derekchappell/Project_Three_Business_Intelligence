# Project Three Business Intelligence #

## Can we create an entire data pipeline from Data procurement to Business Intelligence Tool use? And do it for free? ##

### Here is our basic Architecture ###

[.](<a href="https://imgur.com/cdkegjn"><img src="https://i.imgur.com/cdkegjn.jpg" title="source: imgur.com" /></a>)

### So lets get our Data into the AWS ethosephere ###

[.](https://github.com/derekchappell/Project_Three_Business_Intelligence/blob/main/Photos/S3%20bucket.JPG)
[.](https://github.com/derekchappell/Project_Three_Business_Intelligence/blob/main/Photos/redhsift.JPG)

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
