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

초기 실차 통합에서는 전체 센서를 한 번에 붙이더라도, 문제를 좁히기 위해 LiDAR, TF, pointcloud, localization, GNSS/IMU, Camera 순서로 확인한다.

Autoware 기본 localization은 LiDAR pointcloud와 PCD map 기반 NDT scan matching을 중심으로 동작하며, GNSS와 IMU는 초기 위치 추정, 자세 안정화, pose 보정에 활용된다.
