# Project Three Business Intelligence #



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
