〰️〰️〰️IMAGES - AMAZON〰️〰️〰️〰️〰️〰️〰️〰️〰️
@startuml Images
!include <aws/common>
!include <aws/Storage/AmazonS3/AmazonS3>
!include <aws/Compute/AmazonECR/AmazonECR>
!include <aws/Compute/AmazonECS/AmazonECS>
!include <aws/Compute/AmazonECS/ECScontainer/ECScontainer>
!include <aws/Storage/AmazonS3/bucket/bucket>

AMAZONS3(s3_service, "Amazon S3 Service") {
  BUCKET(site_bucket, "Website Bucket")
  BUCKET(logs_bucket, "Logs Bucket")
}
AMAZONECR(ecr)
AMAZONECS(ecs) {
    ECSCONTAINER(containers, 'Containers', collections)
}
@enduml

〰️〰️〰️〰️IMAGES - AZURE〰️〰️〰️〰️〰️〰️〰️〰️


@startuml

!include <azure/AzureCommon>
!include <azure/Analytics/AzureEventHub>
!include <azure/Analytics/AzureStreamAnalyticsJob>
!include <azure/Databases/AzureCosmosDb>
!include <azure/Databases/AzureCosmosDb>

AzureEventHub(fareDataEventHub, "Fare Data", "PK: Medallion HackLicense VendorId; 3 TUs")
AzureEventHub(tripDataEventHub, "Trip Data", "PK: Medallion HackLicense VendorId; 3 TUs")
AzureStreamAnalyticsJob(streamAnalytics, "Stream Processing", "6 SUs")
AzureCosmosDb(outputCosmosDb, "Output Database", "1,000 RUs")
AzureCosmosDb(outputCosmosDb1, "Output Database", "2,000 RUs")
AzureStreamAnalyticsJob(streamAnalytics2, "Stream Processing", "66 SUs")



@enduml

〰️〰️〰️〰️〰️〰️〰️〰️〰️〰️〰️〰️
