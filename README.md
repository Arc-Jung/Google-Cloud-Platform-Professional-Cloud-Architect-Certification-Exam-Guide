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

https://cloud.google.com/certification/guides/cloud-architect/casestudy-terramearth-rev2

7. [ TerramEarth 사례 연구 / Sample case study: TerramEarth ](https://cloud.google.com/certification/guides/cloud-architect/casestudy-terramearth-rev2) For this question, refer to the TerramEarth case study. To be compliant with European GDPR regulation, TerramEarth is required to delete data generated from its European customers after a period of 36 months when it contains personal data. In the new architecture, this data will be stored in both Cloud Storage and BigQuery. What should you do? 
    -   A. Create a BigQuery table for the European data, and set the table retention period to 36 months. For Cloud Storage, use gsutil to enable lifecycle management using a DELETE action with an Age condition of 36 months. 
    -   B. Create a BigQuery table for the European data, and set the table retention period to 36 months. For Cloud Storage, use gsutil to create a SetStorageClass to NONE action when with an Age condition of 36 months. 
    -   C. Create a BigQuery time-partitioned table for the European data, and set the partition expiration period to 36 months. For Cloud Storage, use gsutil to enable lifecycle management using a DELETE action with an Age condition of 36 months. 
    -   D. Create a BigQuery time-partitioned table for the European data, and set the partition period to 36 months. For Cloud Storage, use gsutil to create a SetStorageClass to NONE action with an Age condition of 36 months. 
    -   Answer: C
    -   36개월이 지나면 데이터를 삭제하도록 묻는 문제이다. 이런 문제는 여러 형태로 나오는데 여기서는 BigQuery의 파티션을 생성할때 파티션의 만료 기간을 36개월로 설정하고 gsutil를 사용하여 JSON을 수정하여 수명 주기를 36개월로 설정하면 된다.
