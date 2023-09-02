# AWS-CLASS-1
import json
def sum_numbers(a,b):
     return a+b
def lambda_handler(event,context):
    print(event)
    print(context)
    print("This is first lamda function !! ")
    print("Sum of a,b is = " ,sum_numbers(2,4))

** READ DATA FROM S3 bucket by Lambda

import json
import boto3
s3 = boto3.resource('s3')

def lambda_handler(event, context):
    # TODO implement
    bucket = s3.Bucket('batch1s3bucket')
    print(bucket.objects.all())
    print("=========================")
    for obj in bucket.objects.all():
        key = obj.key
        print(key)
