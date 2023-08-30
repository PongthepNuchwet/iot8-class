## How do you design MQTT topics and payloads for smart washing machine

1. สถานะเครื่องซักผ้า
   - topic:v1cdti/hw/get/6310301004/model-00/sn-001/
   - topic:v1cdti/hw/set/6310301004/model-00/sn-001/
   - payload
     - {"STATUS": "POWER ON|START|STOP|FINISHED|POWERED OFF"}
     - {"STATUS-WASH": "WASH|SPIN|DRAINED"}
1. เซนเซอร์ภายในเครื่องซักผ้า

   - topic:v1cdti/hw/get/6310301004/model-01/sn-001
   - payload
     - {"temperature": "25.2"}
     - {"pressure": "1013.25"}
     - {"hall": "0" | "1"}
     - {"speed": "100"}
     - {"fabric": "0" | "1"}
     - {"water-flow": "100"}
     - {"water-level": "50"}
     - {"foam": "0" | "1"}
     - {"weight": "value"}
     - {"filter-clogging": "0" | "1"}
     - {"voice-noise": "60" } // dB
     - {"imbalance": "0" | "1"}
     - {"material": "0" | "1"}
     - {"vibration": "0" | "1"}

1. เซนเซอร์ภายนอกเครื่องซักผ้า
   - topic:v1cdti/hw/get/6310301004/model-02/sn-001
   - payload
     - {"3D-Position": "3"}
     - {"Touch": "0" | "1"}
     - {"Lid": "0"| "1"}
     - {"track-people": "0" | "1}
     - {"gesture": "100"}
     - {"barometric-pressure": "100"}
