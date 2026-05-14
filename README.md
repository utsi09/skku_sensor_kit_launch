# skku_sensor_kit_launch

---

common_sensor_launch :

config :

(상황에 따라 수정)

config/* : 공통 sensing pipeline에서 사용하는 센서 전처리 및 driver 관련 파라미터

launch :

(상황에 따라 수정)

launch/* : LiDAR, Camera, GNSS, IMU 등 공통 센서 launch 구성

---

skku_sensor_kit_description :

config :

(수정)

config/sensor_kit_calibration.yaml : sensor kit 전체 calibration 정보

config/sensors_calibration.yaml : LiDAR, Camera, GNSS, IMU의 위치 및 회전값

urdf :

(수정)

urdf/sensor_kit.xacro : sensor kit 전체 프레임 구조

urdf/sensors.xacro : 각 센서 frame 정의 및 base_link와의 연결

---

skku_sensor_kit_launch :

config :

(수정)

config/sensor_kit.param.yaml : sensor kit 전체 파라미터

config/diagnostic_aggregator : 센서 diagnostic aggregation 설정

config/dummy_diag_publisher : dummy diagnostic publisher 설정

launch :

(수정)

launch/lidar.launch.xml : LiDAR sensing launch

launch/camera.launch.xml : Camera sensing launch

launch/gnss.launch.xml : GNSS sensing launch

launch/imu.launch.xml : IMU sensing launch

launch/sensing.launch.xml : 전체 sensing launch

---

