```
{
  "name": "as.up.data.forward",
  "time": "2024-09-27T11:01:46.524679415Z",
  "identifiers": [
    {
      "device_ids": {
        "device_id": "kwiksdevice",
        "application_ids": {
          "application_id": "kwiksapp"
        },
        "dev_eui": "0004A30B0020784D",
        "join_eui": "0303030303030303",
        "dev_addr": "260BBDA4"
      }
    }
  ],
  "data": {
    "@type": "type.googleapis.com/ttn.lorawan.v3.ApplicationUp",
    "end_device_ids": {
      "device_id": "kwiksdevice",
      "application_ids": {
        "application_id": "kwiksapp"
      },
      "dev_eui": "0004A30B0020784D",
      "join_eui": "0303030303030303",
      "dev_addr": "260BBDA4"
    },
    "correlation_ids": [
      "gs:uplink:01J8SJ9PPCNJ0ZF8TF439SR1GS"
    ],
    "received_at": "2024-09-27T11:01:46.521777256Z",
    "uplink_message": {
      "session_key_id": "AZIzGx0b4LKi8oA11Ox66w==",
      "f_port": 1,
      "frm_payload": "Zg==",
      "rx_metadata": [
        {
          "gateway_ids": {
            "gateway_id": "hhs-hboict-nse-delft",
            "eui": "C0EE40FFFF294119"
          },
          "time": "2024-09-27T11:01:46.291042089Z",
          "timestamp": 860786716,
          "rssi": -69,
          "channel_rssi": -69,
          "snr": 6.25,
          "location": {
            "latitude": 52.0019449227654,
            "longitude": 4.3672296126473675,
            "altitude": 8,
            "source": "SOURCE_REGISTRY"
          },
          "uplink_token": "CiIKIAoUaGhzLWhib2ljdC1uc2UtZGVsZnQSCMDuQP//KUEZEJygupoDGgwImqHatwYQ3I7xlgEg4NqL14YZ",
          "received_at": "2024-09-27T11:01:46.304512973Z"
        },
        {
          "gateway_ids": {
            "gateway_id": "eui-58a0cbfffe804e23",
            "eui": "58A0CBFFFE804E23"
          },
          "time": "2024-09-27T11:01:46.256426095Z",
          "timestamp": 3082096756,
          "rssi": -108,
          "channel_rssi": -108,
          "snr": 6.5,
          "location": {
            "latitude": 52.00200284022436,
            "longitude": 4.366765022277833,
            "source": "SOURCE_REGISTRY"
          },
          "uplink_token": "CiIKIAoUZXVpLTU4YTBjYmZmZmU4MDRlMjMSCFigy//+gE4jEPSg1L0LGgwImqHatwYQ79aOmAEgoIqh2tlZ",
          "received_at": "2024-09-27T11:01:46.274387912Z"
        }
      ],
      "settings": {
        "data_rate": {
          "lora": {
            "bandwidth": 125000,
            "spreading_factor": 12,
            "coding_rate": "4/5"
          }
        },
        "frequency": "868100000",
        "timestamp": 860786716,
        "time": "2024-09-27T11:01:46.291042089Z"
      },
      "received_at": "2024-09-27T11:01:46.317322518Z",
      "confirmed": true,
      "consumed_airtime": "1.155072s",
      "network_ids": {
        "net_id": "000013",
        "ns_id": "EC656E0000000181",
        "tenant_id": "ttn",
        "cluster_id": "eu1",
        "cluster_address": "eu1.cloud.thethings.network"
      }
    }
  },
  "correlation_ids": [
    "gs:uplink:01J8SJ9PPCNJ0ZF8TF439SR1GS"
  ],
  "origin": "ip-10-100-7-85.eu-west-1.compute.internal",
  "context": {
    "tenant-id": "CgN0dG4="
  },
  "visibility": {
    "rights": [
      "RIGHT_APPLICATION_TRAFFIC_READ"
    ]
  },
  "unique_id": "01J8SJ9PWWG2KFJ8VC617QTQJW"
}
```


```
sys get ver
RN2483 1.0.5 Oct 31 2018 15:06:52
mac set appeui 0303030303030303
ok
mac get appeui
0303030303030303
mac set appkey E05C89370B4CD40D96537FB9725457D2
ok
mac save
ok
mac join otaa
ok
accepted
mac tx cnf 1 0x66
invalid_param
mac tx cnf 1 66
ok
mac_tx_ok
```