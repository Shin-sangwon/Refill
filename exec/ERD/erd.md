# ERD
| Members                  |                             |                             |                                                                                    |         |                   |                         |   |   |   |   |   |   |
|--------------------------|-----------------------------|-----------------------------|------------------------------------------------------------------------------------|---------|-------------------|-------------------------|---|---|---|---|---|---|
| 키                        | 논리                          | 물리                          | 타입                                                                                 | Null 허용 | 기본값               | 코멘트                     |   |   |   |   |   |   |
| PK                       | member_id                   | member_id                   | BIGINT                                                                             | N       |                   |                         |   |   |   |   |   |   |
|                          | 로그인 아이디                     | loginid                     | VARCHAR(16)                                                                        | N       |                   |                         |   |   |   |   |   |   |
|                          | 비밀번호                        | password                    | VARCHAR(255)                                                                       | N       |                   |                         |   |   |   |   |   |   |
|                          | 닉네임                         | nick_name                   | VARCHAR(8)                                                                         | N       |                   |                         |   |   |   |   |   |   |
|                          | 성명                          | name                        | VARCHAR(10)                                                                        | N       |                   |                         |   |   |   |   |   |   |
|                          | 주소                          | address                     | VARCHAR(255)                                                                       | N       |                   |                         |   |   |   |   |   |   |
|                          | 전화번호                        | phone_number                | VARCHAR(13)                                                                        | N       |                   |                         |   |   |   |   |   |   |
|                          | 생년월일                        | birth                       | DATE                                                                               | N       |                   |                         |   |   |   |   |   |   |
|                          | 이메일                         | email                       | VARCHAR(50)                                                                        | N       |                   |                         |   |   |   |   |   |   |
|                          | 회원 프로필 사진                   | profile_img                 | VARCHAR(255)                                                                       | Y       |                   |                         |   |   |   |   |   |   |
|                          | 역할                          | role                        | ENUM('member', 'admin')                                                            | N       | MEMBER            |                         |   |   |   |   |   |   |
|                          | createdAt                   | createdAt                   | DATETIME                                                                           | N       | CURRENT_TIMESTAMP |                         |   |   |   |   |   |   |
|                          | updatedAt                   | updatedAt                   | DATETIME                                                                           | N       | CURRENT_TIMESTAMP |                         |   |   |   |   |   |   |
|                          |                             |                             |                                                                                    |         |                   |                         |   |   |   |   |   |   |
| Hospitals                |                             |                             |                                                                                    |         |                   |                         |   |   |   |   |   |   |
| 키                        | 논리                          | 물리                          | 타입                                                                                 | Null 허용 | 기본값               | 코멘트                     |   |   |   |   |   |   |
| PK                       | hospital_id                 | hospital_id                 | BIGINT                                                                             | N       |                   |                         |   |   |   |   |   |   |
|                          | 로그인 아이디                     | loginid                     | VARCHAR(16)                                                                        | N       |                   |                         |   |   |   |   |   |   |
|                          | 비밀번호                        | password                    | VARCHAR(255)                                                                       | N       |                   |                         |   |   |   |   |   |   |
|                          | 병원 이름                       | name                        | VARCHAR(255)                                                                       | N       |                   |                         |   |   |   |   |   |   |
|                          | 주소                          | address                     | VARCHAR(255)                                                                       | N       |                   |                         |   |   |   |   |   |   |
|                          | 위도                          | latitude                    | DECIMAL(10, 8)                                                                     | N       |                   |                         |   |   |   |   |   |   |
|                          | 경도                          | longitude                   | DECIMAL(11, 8)                                                                     | N       |                   |                         |   |   |   |   |   |   |
|                          | 우편번호                        | postal_code                 | VARCHAR(255)                                                                       | N       |                   |                         |   |   |   |   |   |   |
|                          | 전화번호                        | phone_number                | VARCHAR(255)                                                                       | N       |                   |                         |   |   |   |   |   |   |
|                          | 역할                          | role                        | ENUM('ROLE_HOSPITAL')                                                              | N       |                   |                         |   |   |   |   |   |   |
|                          | 병원 프로필 사진                   | hospital_profile_img        | VARCHAR(255)                                                                       | N       |                   |                         |   |   |   |   |   |   |
|                          | 병원 배너 사진                    | hospital_banner_img         | VARCHAR(255)                                                                       | N       |                   |                         |   |   |   |   |   |   |
|                          | 병원 등록증 사진                   | registration_img            | VARCHAR(255)                                                                       | N       |                   |                         |   |   |   |   |   |   |
|                          | createdAt                   | createdAt                   | DATETIME                                                                           | N       | CURRENT_DATETIME  |                         |   |   |   |   |   |   |
|                          | updatedAt                   | updatedAt                   | DATETIME                                                                           | N       | CURRENT_DATETIME  |                         |   |   |   |   |   |   |
|                          | 이메일                         | email                       | VARCHAR(255)                                                                       | N       |                   |                         |   |   |   |   |   |   |
|                          |                             |                             |                                                                                    |         |                   |                         |   |   |   |   |   |   |
| Hospital_Operating_Hours |                             |                             |                                                                                    |         |                   |                         |   |   |   |   |   |   |
| 키                        | 논리                          | 물리                          | 타입                                                                                 | Null 허용 | 기본값               | 코멘트                     |   |   |   |   |   |   |
| PK                       | hour_id                     | hour_id                     | BIGINT                                                                             | N       |                   |                         |   |   |   |   |   |   |
| FK                       | hospital_id                 | hospital_id                 | BIGINT                                                                             | N       |                   |                         |   |   |   |   |   |   |
|                          | 요일                          | day_of_week                 | ENUM('Sunday', 'Monday', 'Tuesday', 'Wednesday', 'Thursday', 'Friday', 'Saturday') | N       |                   |                         |   |   |   |   |   |   |
|                          | 시작시간                        | start_time                  | TIME                                                                               | Y       |                   |                         |   |   |   |   |   |   |
|                          | 종료 시간                       | end_time                    | TIME                                                                               | Y       |                   |                         |   |   |   |   |   |   |
|                          | createdAt                   | createdAt                   | DATETIME                                                                           | N       | CURRENT_TIMESTAMP |                         |   |   |   |   |   |   |
|                          | updatedAt                   | updatedAt                   | DATETIME                                                                           | N       | CURRENT_TIMESTAMP |                         |   |   |   |   |   |   |
|                          |                             |                             |                                                                                    |         |                   |                         |   |   |   |   |   |   |
| Doctors                  |                             |                             |                                                                                    |         |                   |                         |   |   |   |   |   |   |
| 키                        | 논리                          | 물리                          | 타입                                                                                 | Null 허용 | 기본값               | 코멘트                     |   |   |   |   |   |   |
| PK                       | doctor_id                   | doctor_id                   | BIGINT                                                                             | N       |                   |                         |   |   |   |   |   |   |
| FK                       | hospital_id                 | hospital_id                 | BIGINT                                                                             | N       |                   |                         |   |   |   |   |   |   |
|                          | 이름                          | name                        | VARCHAR(255)                                                                       | N       |                   |                         |   |   |   |   |   |   |
|                          | 사진                          | profile_img                 | VARCHAR(255)                                                                       | N       |                   |                         |   |   |   |   |   |   |
|                          | 면허번호                        | license_number              | VARCHAR(255)                                                                       | N       |                   |                         |   |   |   |   |   |   |
|                          | 면허사진                        | license_img                 | VARCHAR(255)                                                                       | N       |                   |                         |   |   |   |   |   |   |
|                          | 의사 소개                       | description                 | TEXT                                                                               | N       |                   |                         |   |   |   |   |   |   |
|                          | createdAt                   | createdAt                   | DATETIME                                                                           | N       | CURRENT_DATETIME  |                         |   |   |   |   |   |   |
|                          | updatedAt                   | updatedAt                   | DATETIME                                                                           | N       | CURRENT_DATETIME  |                         |   |   |   |   |   |   |
|                          |                             |                             |                                                                                    |         |                   |                         |   |   |   |   |   |   |
| Education_Background     |                             |                             |                                                                                    |         |                   |                         |   |   |   |   |   |   |
| 키                        | 논리                          | 물리                          | 타입                                                                                 | Null 허용 | 기본값               | 코멘트                     |   |   |   |   |   |   |
| PK                       | education_qualifications_id | education_qualifications_id | BIGINT                                                                             | N       |                   |                         |   |   |   |   |   |   |
| FK                       | doctor_id                   | doctor_id                   | BIGINT                                                                             | N       |                   |                         |   |   |   |   |   |   |
|                          | 내용                          | content                     | TEXT                                                                               | Y       |                   |                         |   |   |   |   |   |   |
|                          | createdAt                   | createdAt                   | DATETIME                                                                           | N       | CURRENT_TIMESTAMP |                         |   |   |   |   |   |   |
|                          | updatedAt                   | updatedAt                   | DATETIME                                                                           | N       | CURRENT_TIMESTAMP |                         |   |   |   |   |   |   |
|                          |                             |                             |                                                                                    |         |                   |                         |   |   |   |   |   |   |
| MajorAreas               |                             |                             |                                                                                    |         |                   |                         |   |   |   |   |   |   |
| 키                        | 논리                          | 물리                          | 타입                                                                                 | Null 허용 | 기본값               | 코멘트                     |   |   |   |   |   |   |
| PK                       | major_treatment_area_id     | major_treatment_area_id     | BIGINT                                                                             | N       |                   |                         |   |   |   |   |   |   |
| FK                       | doctor_id                   | doctor_id                   | BIGINT                                                                             | N       |                   |                         |   |   |   |   |   |   |
|                          | 내용                          | content                     | TEXT                                                                               | Y       |                   |                         |   |   |   |   |   |   |
|                          | createdAt                   | createdAt                   | DATETIME                                                                           | N       | CURRENT_TIMESTAMP |                         |   |   |   |   |   |   |
|                          | updatedAt                   | updatedAt                   | DATETIME                                                                           | N       | CURRENT_TIMESTAMP |                         |   |   |   |   |   |   |
|                          |                             |                             |                                                                                    |         |                   |                         |   |   |   |   |   |   |
| Reservations             |                             |                             |                                                                                    |         |                   |                         |   |   |   |   |   |   |
| 키                        | 논리                          | 물리                          | 타입                                                                                 | Null 허용 | 기본값               | 코멘트                     |   |   |   |   |   |   |
| PK                       | reservations_id             | reservations_id             | BIGINT                                                                             | N       |                   |                         |   |   |   |   |   |   |
| FK                       | member_id                   | member_id                   | BIGINT                                                                             | N       |                   |                         |   |   |   |   |   |   |
| FK                       | doctor_id                   | doctor_id                   | BIGINT                                                                             | N       |                   |                         |   |   |   |   |   |   |
| FK                       | consultations_id            | consultations_id            | BIGINT                                                                             | N       |                   |                         |   |   |   |   |   |   |
|                          | 상담시 요청사항                    | counseling_demands          | VARCHAR(255)                                                                       | Y       |                   |                         |   |   |   |   |   |   |
|                          | 상담 시작시간                     | start_datetime              | DATETIME                                                                           | N       |                   |                         |   |   |   |   |   |   |
|                          | 상담 끝 시간                     | end_datetime                | DATETIME                                                                           | N       |                   |                         |   |   |   |   |   |   |
|                          | 취소여부                        | is_canceled                 | TINYINT                                                                            | N       |                   |                         |   |   |   |   |   |   |
|                          | 사진                          | hair_image                  | VARCHAR(255)                                                                       | N       |                   |                         |   |   |   |   |   |   |
|                          | createdAt                   | createdAt                   | DATETIME                                                                           | N       | CURRENT_DATETIME  |                         |   |   |   |   |   |   |
|                          | updatedAt                   | updatedAt                   | DATETIME                                                                           | N       | CURRENT_DATETIME  |                         |   |   |   |   |   |   |
|                          |                             |                             |                                                                                    |         |                   |                         |   |   |   |   |   |   |
| AI_Diagnosis             |                             |                             |                                                                                    |         |                   |                         |   |   |   |   |   |   |
| 키                        | 논리                          | 물리                          | 타입                                                                                 | Null 허용 | 기본값               | 코멘트                     |   |   |   |   |   |   |
| PK                       | ai_diagnosis_id             | ai_diagnosis_id             | BIGINT                                                                             | N       |                   |                         |   |   |   |   |   |   |
| FK                       | member_id                   | member_id                   | BIGINT                                                                             | N       |                   |                         |   |   |   |   |   |   |
|                          | 사진                          | diagnosisImage              | VARCHAR(255)                                                                       | N       |                   |                         |   |   |   |   |   |   |
|                          | 설문결과                        | survey_results              | TEXT                                                                               | N       |                   | 설문 항목들을 (01011..)식으로 저장 |   |   |   |   |   |   |
|                          | 진단타입                        | hair_loss_type              | ENUM(1,2,3,4,5,6,7)                                                                | Y       |                   |                         |   |   |   |   |   |   |
|                          | 진단결과                        | diagnosis_results           | TEXT                                                                               | N       |                   |                         |   |   |   |   |   |   |
|                          | createdAt                   | createdAt                   | DATETIME                                                                           | N       | CURRENT_TIMESTAMP |                         |   |   |   |   |   |   |
|                          | updatedAt                   | updatedAt                   | DATETIME                                                                           | N       | CURRENT_TIMESTAMP |                         |   |   |   |   |   |   |
|                          | 진단 점수                       | hair_loss_score             | BIGINT                                                                             | Y       |                   |                         |   |   |   |   |   |   |
|                          | 확신도                         | certainty                   | VARCHAR(100)                                                                       | N       |                   |                         |   |   |   |   |   |   |
|                          | 머리 여부확인                     | model_confidence            | VARCHAR(100)                                                                       | N       |                   |                         |   |   |   |   |   |   |
|                          |                             |                             |                                                                                    |         |                   |                         |   |   |   |   |   |   |
| Reviews                  |                             |                             |                                                                                    |         |                   |                         |   |   |   |   |   |   |
| 키                        | 논리                          | 물리                          | 타입                                                                                 | Null 허용 | 기본값               | 코멘트                     |   |   |   |   |   |   |
| PK                       | reviews_id                  | reviews_id                  | BIGINT                                                                             | N       |                   |                         |   |   |   |   |   |   |
| FK                       | member_id                   | member_id                   | BIGINT                                                                             | N       |                   |                         |   |   |   |   |   |   |
| FK                       | doctor_id                   | doctor_id                   | BIGINT                                                                             | N       |                   |                         |   |   |   |   |   |   |
| FK                       | hospital_id                 | hospital_id                 | BIGINT                                                                             | N       |                   |                         |   |   |   |   |   |   |
|                          | 별점                          | score                       | INT                                                                                | N       |                   |                         |   |   |   |   |   |   |
|                          | 내용                          | content                     | TEXT                                                                               | N       |                   |                         |   |   |   |   |   |   |
|                          | createdAt                   | createdAt                   | DATETIME                                                                           | N       | CURRENT_TIMESTAMP |                         |   |   |   |   |   |   |
|                          | updatedAt                   | updatedAt                   | DATETIME                                                                           | N       | CURRENT_TIMESTAMP |                         |   |   |   |   |   |   |
|                          | 신고 여부                       | isblocked                   | TINYINT                                                                            | N       | FALSE             |                         |   |   |   |   |   |   |
|                          |                             |                             |                                                                                    |         |                   |                         |   |   |   |   |   |   |
| Consulting               |                             |                             |                                                                                    |         |                   |                         |   |   |   |   |   |   |
| 키                        | 논리                          | 물리                          | 타입                                                                                 | Null 허용 | 기본값               | 코멘트                     |   |   |   |   |   |   |
| PK                       | consulting_id               | consulting_id               | BIGINT                                                                             | N       |                   |                         |   |   |   |   |   |   |
| FK                       | member_id                   | member_id                   | BIGINT                                                                             | N       |                   |                         |   |   |   |   |   |   |
| FK                       | doctor_id                   | doctor_id                   | BIGINT                                                                             | N       |                   |                         |   |   |   |   |   |   |
|                          | 방 이름                        | room_name                   | VARCHAR(255)                                                                       | Y       |                   |                         |   |   |   |   |   |   |
|                          | 상담 소요시간                     | consumption_time            | TIME                                                                               | Y       |                   |                         |   |   |   |   |   |   |
|                          | createdAt                   | createdAt                   | DATETIME                                                                           | N       | CURRENT_TIMESTAMP |                         |   |   |   |   |   |   |
|                          | updatedAt                   | updatedAt                   | DATETIME                                                                           | N       | CURRENT_TIMESTAMP |                         |   |   |   |   |   |   |
|                          | 세션번호                        | session_id                  | VARCHAR(255)                                                                       | N       |                   |                         |   |   |   |   |   |   |
|                          | 회원토큰                        | member_token                | VARCHAR(255)                                                                       | N       |                   |                         |   |   |   |   |   |   |
|                          | 의사토큰                        | doctor_token                | VARCHAR(255)                                                                       | N       |                   |                         |   |   |   |   |   |   |
|                          | 화면공유토큰                      | screen_share_token          | VARCHAR(255)                                                                       | N       |                   |                         |   |   |   |   |   |   |
|                          | 상담 정보                       | consulting_detail_info      | VARCHAR(255)                                                                       | N       |                   |                         |   |   |   |   |   |   |
|                          | 상담 여부                       | is_excuted                  | TINYINT                                                                            | N       |                   |                         |   |   |   |   |   |   |
|                          |                             |                             |                                                                                    |         |                   |                         |   |   |   |   |   |   |
| Report                   |                             |                             |                                                                                    |         |                   |                         |   |   |   |   |   |   |
| 키                        | 논리                          | 물리                          | 타입                                                                                 | Null 허용 | 기본값               | 코멘트                     |   |   |   |   |   |   |
| PK                       | report_id                   | report_id                   | BIGINT                                                                             | N       |                   |                         |   |   |   |   |   |   |
| FK                       | member_id                   | member_id                   | BIGINT                                                                             | N       |                   |                         |   |   |   |   |   |   |
| FK                       | doctor_id                   | doctor_id                   | BIGINT                                                                             | N       |                   |                         |   |   |   |   |   |   |
| FK                       | 상담_아이디                      | consultations_id            | BIGINT                                                                             | N       |                   |                         |   |   |   |   |   |   |
|                          | 내용                          | content                     | TEXT                                                                               | Y       |                   |                         |   |   |   |   |   |   |
|                          |                             |                             |                                                                                    |         |                   |                         |   |   |   |   |   |   |
| complaint                |                             |                             |                                                                                    |         |                   |                         |   |   |   |   |   |   |
| 키                        | 논리                          | 물리                          | 타입                                                                                 | Null 허용 | 기본값               | 코멘트                     |   |   |   |   |   |   |
| PK                       | complaint_id                | complaint_id                | BIGINT                                                                             | N       |                   |                         |   |   |   |   |   |   |
|                          | 신고자 유형                      | reporter_role               | VARCHAR(100)                                                                       | Y       |                   |                         |   |   |   |   |   |   |
|                          | 신고자 아이디                     | reporter_id                 | BIGINT                                                                             | Y       |                   |                         |   |   |   |   |   |   |
|                          | 신고된 타겟 아이디                  | target_id                   | BIGINT                                                                             | Y       |                   |                         |   |   |   |   |   |   |
|                          | 신고된 타겟 타입                   | target_type                 | VARCHAR(100)                                                                       | Y       |                   |                         |   |   |   |   |   |   |
|                          | 신고 내용                       | content                     | TEXT                                                                               | N       |                   |                         |   |   |   |   |   |   |
|                          |                             |                             |                                                                                    |         |                   |                         |   |   |   |   |   |   |
| Doctor_Biography         |                             |                             |                                                                                    |         |                   |                         |   |   |   |   |   |   |
| 키                        | 논리                          | 물리                          | 타입                                                                                 | Null 허용 | 기본값               | 코멘트                     |   |   |   |   |   |   |
| PK                       | 의사약력_아이디                    | doctor_biography_id         | BIGINT                                                                             | N       |                   |                         |   |   |   |   |   |   |
|                          | 약력 내용                       | content                     | TEXT                                                                               | Y       |                   |                         |   |   |   |   |   |   |
|                          | createdAt                   | createdAt                   | DATETIME                                                                           | N       | CURRENT_TIMESTAMP |                         |   |   |   |   |   |   |
|                          | updatedAt                   | updatedAt                   | DATETIME                                                                           | N       | CURRENT_TIMESTAMP |                         |   |   |   |   |   |   |
|                          |                             |                             |                                                                                    |         |                   |                         |   |   |   |   |   |   |