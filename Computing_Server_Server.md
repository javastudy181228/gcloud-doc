# Computing_Server_Server_시작.md

## 기능
1. 서버 생성 기능
2. 티어 조회
3. 네트워크 조회

### URL
- https://cloud.kt.com/console/d/osserver

### Source
- src.ktcloudportal/epc.servlet.osSvcSvrProcess.java
- WebContent/d/console/console.iaas.osserver.jsp
- WebContent/d/scripts/console.iaas.osserver.js

### Database
- TBMB_
- PROCEDURE...
- FUNCTION...

### API List
- https://~//nova/v2.1/servers/details

```
-- curl 호출
curl -v -X GET -H 'Content-Type: application/json' 
-H 'Authorization: loginId' 
-H 'X-Auth-Token: gAAAAABiMFuKkTYaoM3bpyL1vz25v46yze37exfDTKNgj3PJcy-Ki8J5KwFrnV_hJ9CH51w7B2VNn0lHU192aLsVvWJxzcLlYfdqKiFuCLGAhwzpJkhIHs7RRUtv0eaeEuNqsmb25QRnt228s4lNpzJiKJu7JZeyzc9pWi48m_BW-4XImH3TlBg' 
'http://210.106.96.161:8080/rdbaas-management/v2/mysql/instances?instanceIds=04f860b3-ab80-4414-9c45-0fd2acbdc7b0'

-- 응답값
 {
  "listInstancesResponse": {
    "jobId": "71129f95-08fd-42c7-8d93-da6bc7127cd3",
    "instanceList": [
      {
        "instanceId": "04f860b3-ab80-4414-9c45-0fd2acbdc7b0",
        "perfClass": "f9764e6b-1b46-421d-8998-816c2d8d13ce",
        "vmTemplateId": 1,
        "dbParamGroupId": "21",
        "userRegNo": "f77155e6-e58e-4c96-ab39-219e6d267724",
        "instanceType": "DEFAULT",
        "instanceName": "khkrecover006",
        "instanceStatus": "CREATING",
        "instanceCreationTime": null,
        "instanceUpdateTime": null,
        "backupStartHour": 2,
        "backupStartMin": 0,
        "backupRetention": 0,
        "backupDuration": 2,
        "maintenanceWeekDay": "MON",
        "maintenanceStartHour": 3,
        "maintenanceStartMin": 0,
        "maintenanceDuration": 4,
        "storageSize": 80,
        "dbMasterName": "khkadmin",
        "dbName": "khktestdb",
        "dbVersionId": 4,
        "needReboot": "YES",
        "vmId": "7509e6c2-e111-4d48-a80b-d78fb13275ae",
        "privateIpAddress": "172.25.0.71",
        "privateDbPort": 3306,
        "publicIpAddress": "210.106.96.160",
        "publicDbPort": 31006,
        "publicSshPort": 31106,
        "relationshipType": "BACKUP_ORIGINAL",
        "relationshipTarget": "68ac3a32-bb30-4bab-872d-0b3d197c2d52",
        "zoneName": "DX-M1",
        "tierName": "ced3efb8-1b8f-47e1-8fc9-62fad29cc258",
        "dbVersionName": "5.6.24",
        "dbParamGroupName": "mysql5.6.24_default",
        "accessControlGroupIds": [],
        "dataVolumeId": null,
        "storageType": null,
        "iops": null
      }
    ],
    "count": 1
  }
}  
```

### VOC 이력 ??
- 2022.