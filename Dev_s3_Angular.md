# Running an angular application on an S3 bucket in AWS

## check versions
- `node -v`
- `npm -v`  
- `ng --version`
## Build
- `ng build`
- files in dist/ folder webpacked app
## Login to AWS
- navigate to S3/bucket create Bucket name lowercase-with-dash
- make public, acknolege with checkbox, click --create bucket
- navigate into the bucket--click upload
- upload the files the folder inside the dist folder
- --upload, --close
### Deploy
- Go to Properties, scroll to the bottom: Static webhosting set to enable
- set index.html page --save changes
- now lists the bucket website endpoint
- set to forbiden so change the objects to public 
- May need to manually set ACLs changes to ownership enforcement enabled
- navigate to endpoint




