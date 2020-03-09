1.  A lead software engineer tells you that his new application design uses websockets and HTTP sessions that are not distributed across the web servers. You want to help him ensure his application will run property on Google Cloud Platform. What should you do? 

    -   A. Help the engineer to convert his websocket code to use HTTP streaming. 
    -   B. Review the encryption requirements for websocket connections with the security team. 
    -   C. Meet with the cloud operations team and the engineer to discuss load balancer options. 
    -   D. Help the engineer redesign the application to use a distributed user session service that does not rely on websockets and HTTP sessions. 
    -   Answer: C
    -  websockets, HTTP 세션을 사용하는 웹 어플리케이션이면 로드 밸런스를 통하여 웹서버로 올바르게 분배시켜줘야 한다.

2.  You are helping the QA team to roll out a new load-testing tool to test the scalability of your primary cloud services that run on Google Compute Engine with Cloud Bigtable. Which three requirements should they include? Choose 3 answers 
    -   A. Ensure that the load tests validate the performance of Cloud Bigtable. 
    -   B. Create a separate Google Cloud project to use for the load-testing environment. 
    -   C. Schedule the load-testing tool to regularly run against the production environment. 
    -   D. Ensure all third-party systems your services use are capable of handling high load. 
    -   E. Instrument the production services to record every transaction for replay by the load-testing tool. 
    -   F. Instrument the load-testing tool and the target services with detailed logging and metrics collection. 
    -   Answer: BCD
    -   Bigtable 을 테스트 할때 3가지의 요구사항을 찾는 문제이다. GCP에서는 테스트 용도의 별도의 프로젝트를 생성하라고 가이드를 주고 있다. 또한 Bigtable의 경우 Bigtable의 부하로 인하여 다른 어플리케이션에서 문제를 일으키는 경우가 있어서 확인해야 한다. 테스트 용도의 별도의 프로젝트를 생성하였으면 그 프로젝트에 주기적으로 부하를 주면서 실험해야 한다. 

3. You need to ensure reliability for your application and operations by supporting reliable task a scheduling for compute on GCP. Leveraging Google best practices, what should you do? 
    -   A. Using the Cron service provided by App Engine, publishing messages directly to a messageprocessing utility service running on Compute Engine instances. 
    -   B. Using the Cron service provided by App Engine, publish messages to a Cloud Pub/Sub topic. Subscribe to that topic using a message-processing utility service running on Compute Engine instances. 
    -   C. Using the Cron service provided by Google Kubernetes Engine (GKE), publish messages directly to a message-processing utility service running on Compute Engine instances. 
    -   D. Using the Cron service provided by GKE, publish messages to a Cloud Pub/Sub topic. Subscribe to that topic using a message-processing utility service running on Compute Engine instances. 
    -   Answer: B  
    -   App Engine의 Cron을 사용하여서 Cloud Pub/Sub로 메세지를 주기적으로 보내는 것이 좋다. 다른 보기들은 직접 작성한다고 해서 오답이고, D의 경우 GKE(Google Kubernetes Engine)의 경우에는 GCP의 기능이 아닌 외부 모니터링 어플리케이션을 설치해야함으로 권장되는 항목이 아니다.


4. You are migrating your on-premises solution to Google Cloud in several phases. You will use Cloud VPN to maintain a connection between your on-premises systems and Google Cloud until the migration is completed. You want to make sure all your on-premises systems remain reachable during this period. How should you organize your networking in Google Cloud? 
    -   A. Use the same IP range on Google Cloud as you use on-premises 
    -   B. Use the same IP range on Google Cloud as you use on-premises for your primary IP range and use a secondary range that does not overlap with the range you use on-premises 
    -   C. Use an IP range on Google Cloud that does not overlap with the range you use on-premises 
    -   D. Use an IP range on Google Cloud that does not overlap with the range you use on-premises for your primary IP range and use a secondary range with the same IP range as you use on- premises 
    -   Answer: D
    -   온프레미스에서 클라우드로 이동하는 경우에 발생하는 문제에 대해 묻는 문제이다.  Cloud VPN을 통해서 기존 온프레미스의 서버에 접속을 유지 하면서 클라우드 서비스를 만들고 싶은 경우 기존 온프레미스 서버의 IP 주소 범위를 먼저 지정하고, 겹치지 않도록 주의 하면서 세컨더리 IP를 클라우드 서비스를 할당하면 된다.

5. Your company creates rendering software which users can download from the company website. Your company has customers all over the world. You want to minimize latency for all your customers. You want to follow Google-recommended practices. How should you store the files? 
   -   A. Save the files in a Multi-Regional Cloud Storage bucket. 
   -   B. Save the files in a Regional Cloud Storage bucket, one bucket per zone of the region.
   -   C. Save the files in multiple Regional Cloud Storage buckets, one bucket per zone per region. 
   -   D. Save the files in multiple Multi-Regional Cloud Storage buckets, one bucket per multi-region. 
   -   Answer: D
   -   전세계에서 접속하는 다운로드의 경우 멀티 리전 버켓을 사용해야한다. 이 문제에서는 각 도시의 리전들을 묶어 대륙단위의 아시아, 유럽, 북미에 있는 멀티 리전 서비스를 다시 한번 묶어서 사용하면 더 폭 넓게 구성할 수 있다는 것을 알려주는 문제이다.

6. You need to develop procedures to verify resilience of disaster recovery for remote recovery using GCP. Your production environment is hosted on-premises. You need to establish a secure, redundant connection between your on premises network and the GCP network. What should you do? 
    -   A. Verify that Dedicated Interconnect can replicate files to GCP. Verify that direct peering can establish a secure connection between your networks if Dedicated Interconnect fails. 
    -   B. Verify that Dedicated Interconnect can replicate files to GCP. Verify that Cloud VPN can establish a secure connection between your networks if Dedicated Interconnect fails.
    -   C. Verify that the Transfer Appliance can replicate files to GCP. Verify that direct peering can establish a secure connection between your networks if the Transfer Appliance fails. 
    -   D. Verify that the Transfer Appliance can replicate files to GCP. Verify that Cloud VPN can establish a secure connection between your networks if the Transfer Appliance fails. 
    -   Answer: A
    -   Dedicated Interconnect를 연결하는 것이 가장 베스트이고 내부망 연결을 위해 외부에 노출되는 방식인 Cloud VPN 방식보단 direct peering를 사용하면 보안을 유지하면서 통신할 수 있다.

7. [ TerramEarth 사례 연구 / Sample case study: TerramEarth ](https://cloud.google.com/certification/guides/cloud-architect/casestudy-terramearth-rev2) For this question, refer to the TerramEarth case study. To be compliant with European GDPR regulation, TerramEarth is required to delete data generated from its European customers after a period of 36 months when it contains personal data. In the new architecture, this data will be stored in both Cloud Storage and BigQuery. What should you do? 
    -   A. Create a BigQuery table for the European data, and set the table retention period to 36 months. For Cloud Storage, use gsutil to enable lifecycle management using a DELETE action with an Age condition of 36 months. 
    -   B. Create a BigQuery table for the European data, and set the table retention period to 36 months. For Cloud Storage, use gsutil to create a SetStorageClass to NONE action when with an Age condition of 36 months. 
    -   C. Create a BigQuery time-partitioned table for the European data, and set the partition expiration period to 36 months. For Cloud Storage, use gsutil to enable lifecycle management using a DELETE action with an Age condition of 36 months. 
    -   D. Create a BigQuery time-partitioned table for the European data, and set the partition period to 36 months. For Cloud Storage, use gsutil to create a SetStorageClass to NONE action with an Age condition of 36 months. 
    -   Answer: C
    -   36개월이 지나면 데이터를 삭제하도록 묻는 문제이다. 이런 문제는 여러 형태로 나오는데 여기서는 BigQuery의 파티션을 생성할때 파티션의 만료 기간을 36개월로 설정하고 gsutil를 사용하여 JSON을 수정하여 수명 주기를 36개월로 설정하면 된다.

8. The application reliability team at your company this added a debug feature to their backend service to send all server events to Google Cloud Storage for eventual analysis. The event records are at least 50 KB and at most 15 MB and are expected to peak at 3,000 events per second. You want to minimize data loss.
Which process should you implement?
   - A. "¢ Append metadata to file body "¢ Compress individual files "¢ Name files with serverName "" Timestamp "¢ Create a new bucket if bucket is older than 1 hour and save individual files to the new bucket. Otherwise, save files to existing bucket.
    - B. "¢ Batch every 10,000 events with a single manifest file for metadata "¢ Compress event files and manifest file into a single archive file "¢ Name files using serverName "" EventSequence "¢ Create a new bucket if bucket is older than 1 day and save the single archive file to the new bucket. Otherwise, save the single archive file to existing bucket.
    - C. "¢ Compress individual files "¢ Name files with serverName "" EventSequence "¢ Save files to one bucket "¢ Set custom metadata headers for each object after saving
    - D. "¢ Append metadata to file body "¢ Compress individual files "¢ Name files with a random prefix pattern "¢ Save files to one bucket

9. You want to make a copy of a production Linux virtual machine in the US-Central region. You want to manage and replace the copy easily if there are changes on the production virtual machine. You will deploy the copy as a new instance in a different project in the US-East region.
What steps must you take?
 - A. Use the Linux dd and netcat commands to copy and stream the root disk contents to a new virtual machine instance in the US-East region.
 - B. Create a snapshot of the root disk and select the snapshot as the root disk when you create a new virtual machine instance in the US-East region.
 - C. Create an image file from the root disk with Linux dd command, create a new virtual machine instance in the US-East region
 - D. Create a snapshot of the root disk, create an image file in Google Cloud Storage from the snapshot, and create a new virtual machine instance in the US-East region using the image file the root disk.

Your company runs several databases on a single MySQL instance. They need to take backups of a specific database at regular intervals. The backup activity needs to complete as quickly as possible and cannot be allowed to impact disk performance.
How should you configure the storage?
A. Configure a cron job to use the gcloud tool to take regular backups using persistent disk snapshots.
B. Mount a Local SSD volume as the backup location. After the backup is complete, use gsutil to move the backup to Google Cloud Storage.
C. Use gcsfise to mount a Google Cloud Storage bucket as a volume directly on the instance and write backups to the mounted location using mysqldump.
D. Mount additional persistent disk volumes onto each virtual machine (VM) instance in a RAID10 array and use LVM to create snapshots to send to Cloud Storage
Correct Answer: C
References:
https://github.com/mvarrieur/MySQL-backup-to-Google-Cloud-Storage https://cloud.google.com/storage/docs/gcs-fuse

Your marketing department wants to send out a promotional email campaign. The development team wants to minimize direct operation management. They project a wide range of possible customer responses, from 100 to 500,000 click-through per day. The link leads to a simple website that explains the promotion and collects user information and preferences.
Which infrastructure should you recommend? Choose 2 answers.
A. Use Google App Engine to serve the website and Google Cloud Datastore to store user data.
B. Use a Google Container Engine cluster to serve the website and store data to persistent disk.
C. Use a managed instance group to serve the website and Google Cloud Bigtable to store user data.
D. Use a single Compute Engine virtual machine (VM) to host a web server, backend by Google Cloud SQL.
Correct Answer: AC

The operations manager asks you for a list of recommended practices that she should consider when migrating a J2EE application to the cloud.
Which three practices should you recommend? Choose 3 answers.
A. Port the application code to run on Google App Engine
B. Integrate Cloud Dataflow into the application to capture real-time metrics
C. Instrument the application with a monitoring tool like Stackdriver Debugger
D. Select an automation framework to reliably provision the cloud infrastructure
E. Deploy a continuous integration tool with automated testing in a staging environment
F. Migrate from MySQL to a managed NoSQL database like Google Cloud Datastore or Bigtable
Correct Answer: ADE

To reduce costs, the Director of Engineering has required all developers to move their development infrastructure resources from on-premises virtual machines
(VMs) to Google Cloud Platform. These resources go through multiple start/stop events during the day and require state to persist. You have been asked to design the process of running a development environment in Google Cloud while providing cost visibility to the finance department.
Which two steps should you take? Choose 2 answers.
A. Use the - -no-auto-delete flag on all persistent disks and stop the VM
B. Use the - -auto-delete flag on all persistent disks and terminate the VM
C. Apply VM CPU utilization label and include it in the BigQuery billing export
D. Use Google BigQuery billing export and labels to associate cost to groups
E. Store all state into local SSD, snapshot the persistent disks, and terminate the VM
F. Store all state in Google Cloud Storage, snapshot the persistent disks, and terminate the VM
 
Correct Answer: CE
C: Billing export to BigQuery enables you to export your daily usage and cost estimates automatically throughout the day to a BigQuery dataset you specify.
Labels applied to resources that generate usage metrics are forwarded to the billing system so that you can break down your billing charges based upon label criteria. For example, the Compute Engine service reports metrics on VM instances. If you deploy a project with 2,000 VMs, each of which is labeled distinctly, then only the first 1,000 label maps seen within the 1 hour window will be preserved.
E: You cannot stop an instance that has a local SSD attached. Instead, you must migrate your critical data off of the local SSD to a persistent disk or to another instance before you delete the instance completely.
You can stop an instance temporarily so you can come back to it at a later time. A stopped instance does not incur charges, but all of the resources that are attached to the instance will still be charged. Alternatively, if you are done using an instance, delete the instance and its resources to stop incurring charges.
References:
https://cloud.google.com/billing/docs/how-to/export-data-bigquery https://cloud.google.com/compute/docs/instances/stopping-or-deleting-an-instance

You write a Python script to connect to Google BigQuery from a Google Compute Engine virtual machine. The script is printing errors that it cannot connect to
BigQuery.
What should you do to fix the script?
A. Install the latest BigQuery API client library for Python
B. Run your script on a new virtual machine with the BigQuery access scope enabled
C. Create a new service account with BigQuery access and execute your script with that user
D. Install the bq component for gcloud with the command gcloud components install bq.
 
Correct Answer: A
Applications that use BigQuery must be associated with a Google Cloud Platform Console project with the BigQuery API enabled.
Reference:
https://cloud.google.com/bigquery/create-simple-app-api

A production database virtual machine on Google Compute Engine has an ext4-formatted persistent disk for data files. The database is about to run out of storage space.
How can you remediate the problem with the least amount of downtime?
A. In the Cloud Platform Console, increase the size of the persistent disk and use the resize2fs command in Linux.
B. Shut down the virtual machine, use the Cloud Platform Console to increase the persistent disk size, then restart the virtual machine
C. In the Cloud Platform Console, increase the size of the persistent disk and verify the new space is ready to use with the fdisk command in Linux
D. In the Cloud Platform Console, create a new persistent disk attached to the virtual machine, format and mount it, and configure the database service to move the files to the new disk
E. In the Cloud Platform Console, create a snapshot of the persistent disk restore the snapshot to a new larger disk, unmount the old disk, mount the new disk and restart the database service
 
Correct Answer: A
On Linux instances, connect to your instance and manually resize your partitions and file systems to use the additional disk space that you added.
Extend the file system on the disk or the partition to use the added space. If you grew a partition on your disk, specify the partition. If your disk does not have a partition table, specify only the disk ID. sudo resize2fs /dev/[DISK_ID][PARTITION_NUMBER] where [DISK_ID] is the device name and [PARTITION_NUMBER] is the partition number for the device where you are resizing the file system.
References:
https://cloud.google.com/compute/docs/disks/add-persistent-disk

