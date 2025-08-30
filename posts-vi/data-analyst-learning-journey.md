---
type: Post
title: Những Gì Mình Đã Học Để Đi Làm Data Analyst
description: >-
  Hành trình học Data Analyst từ xuất phát điểm dân kinh doanh, cách mình học code, tham gia khóa học, luyện SQL và xây dựng portfolio để xin việc.
date: '2024-12-01'
---
## Background Của Mình

Trước khi đi vào cách mình học, mình muốn đề cập đến **background** cá nhân.  
- Mình tốt nghiệp Cử Nhân Khoa Học ngành Quản trị kinh doanh Toàn Cầu của **Troy University**.  
- Học các môn: Phân tích và Quản lý kinh doanh, Kinh tế học, Xác suất thống kê, Quản trị, Kế toán, Marketing,...  
- Thậm chí còn học cả **Machine Learning** (sử dụng AzureML Studio và AWS SageMaker, không cần code).

Nghe ảo quá đúng không. Quản trị kinh doanh mà đi dạy Machine learning 😄 Ở đại học, bọn mình được dạy về ML để có thể ứng dụng các dịch vụ như Microsoft AzureML Studio hay AWS SageMaker. Các dịch vụ Machine Learning này được Microsoft / Amazon setup sẵn hết rồi, không cần biết code vẫn xài được. Quan trọng là phải biết cách chọn thuật toán và tỉnh chỉnh để đạt hiệu quả cao.

Mục đích là dùng các tool này để forecast, dự đoán các chỉ số như Revenue, Customer Churn rate, Delivery Time,… hoặc thực hiện các task phân loại (classification) hay clustering trong marketing, hoặc đơn giản là tự động hoá một vài tác vụ trong kinh doanh.

<img width="3334" height="2048" alt="6165564_Screen_Shot_2022-10-15_at_15 12 54" src="https://github.com/user-attachments/assets/c9a90546-ce24-4bd2-8ff2-aa41ae50ccba" />

Sinh viên được tự pick vài course về Information System.

Với background đó + gần 4 năm mình mở công ty riêng kinh doanh ở lĩnh vực sản xuất và bán lẻ. Mình tự setup website bán hàng, setup web-base ERP (đồ WordPress mua về sửa lại thôi, không có gì thần thánh 😄), thiết kế hệ thống integration để đổ data từ các kênh e-com về. Xuất excel để phân tích và làm báo cáo. Các máy móc trong xưởng mình cũng tìm cách quản lý bằng spreadsheet và kỹ thuật Statistical Process Control.

=> Mình có nền tảng về kinh doanh và giải quyết các vấn đề kinh doanh, ở mức độ non-code (thuần kinh doanh). Mình chỉ thiếu kiến thức ở các tool hay dùng trong data.

---

## Mình đi học code

Công thức của Data Analyst rất đơn giản:  
**Data skill + toán (không cao siêu như toán cao cấp đâu) + Domain knowledge.**  
Bạn nào mạnh về kinh doanh hoặc kiến thức về ngành bạn sắp làm data thì coi như là có ưu thế rồi.

### Quá trình mình học Data của mình thế này:

- Học trên CodeCademy: Cái này là do không có ai định hướng nên học đại, toàn ở beginner – intermediate level
  - Python programming (OOP, lambda function, A/B testing with SciPy…)
  - SQL
  - HTML + CSS (mấy cái này thực ra hồi xưa có biết rồi, học lại thôi)
  - JS + framework Flask, VUE, Bootstrap (beginner)
- Học Data Science ở DataCamp => Không đạt

Đầu tháng 5, mình đăng ký tài khoản DataCamp để mình học (tại vì nó rẻ và thiên hướng data hơn). DataCamp là một nơi rất tốt để bổ sung technical skill, trải nghiệm hand-on, cầm tay chỉ việc là rất tuyệt vời. Nói rút gọn thì Datacamp sẽ giúp bạn trả lời câu hỏi “Tôi phải xử lý vấn đề này thế nào”. Tuy nhiên họ quá tập trung vào tech, không giải thích ý nghĩa, làm cho người mới học trở nên mơ hồ.

> QUẢNG CÁO

Chính vì nó mơ hồ nên mình không hiểu được bức tranh toàn cảnh => Không đạt mục tiêu thi Certificate dù skill gì trong cái course đó cũng biết

<img width="3490" height="2048" alt="6165566_Screen_Shot_2022-10-15_at_14 20 38" src="https://github.com/user-attachments/assets/777652f3-9beb-4c04-a192-8e1ccb24a5af" />


**Khoá Data Scientist của DataCamp**

#### Những thứ mình học

- Python programming (học lại cho nó thấm)
- Pandas + Numpy
- Matplotlib + Seaborn
- PostgreSQL
- Tableau (lúc trước có dùng rồi mà sau này mới học sâu hơn)
- Exploratory Data Analysis (Read, clean, validate, distribution, multivariate relationship, …)
- Statistic in Python
- Scipy
- Scikit-learn

**Các món đã học ở đại học nhưng học lại trên python**

- Hypothesis testing
- Unsupervised, supervised, reinforcement learning, clustering,..

Đây là những gì DataCamp yêu cầu
<img width="1920" height="1508" alt="6165597_Screen_Shot_2022-10-15_at_15 19 08" src="https://github.com/user-attachments/assets/675c9480-82ce-4269-8803-ae76332185dd" />


---

### Học các chứng chỉ của Google Data Analytics trên Coursera

Mãi đến cuối tháng 7, xin được cái học bổng của Google để học toàn bộ khoá học của họ trên Coursera. Khoá học này thì quá cơ bản, chỉ là giới thiệu chung chung. Nhưng nhờ khoá học này mà mình kết nối được các mảnh ghép rời rạc của bức tranh. Nó giúp mình trả lời được câu hỏi “Tại sao tôi phải làm vậy? Tại sao loài người lại nghĩ ra thứ này, và vì sao họ dùng nó trong những trường hợp này”

![6165603_Google_Data_Analytics](https://github.com/user-attachments/assets/95523bef-d812-4e12-8c97-aca50e0baaac)


Khoá học này thì mình học khoảng 4 ngày là xong (thấy Google ghi là học cỡ 6 tháng 😁 nhưng tôi đã quá đau khổ với DataCamp rồi, dăm ba khoá học này ăn nhằm gì). Học nhanh là do học trên DataCamp trước rồi mà chưa hiểu, chứ không phải thiên gì gì đâu nhé anh em.

---

### Trở lại học Datacamp

Sau khi đã có câu trả lời cho câu hỏi “Tại sao tôi phải làm vậy”, mình kết hợp với “Tôi phải xử lý vấn đề này thế nào” => Mình trở lại lấy professional certificate của Datacamp, nhưng là Data Analyst thôi. Mình biết là mình còn thiếu quá nhiều kiến thức để thi Data Scientist nên mình vẫn đang học tiếp.

<img width="1100" height="632" alt="6165601_DA0010562973437" src="https://github.com/user-attachments/assets/e5929608-bd47-4902-b0eb-47d20062ef04" />


Đây là những gì bạn phải đạt khi muốn thành Certified Data Analyst của DataCamp

<img width="3082" height="2048" alt="6165598_Screen_Shot_2022-10-15_at_13 52 14" src="https://github.com/user-attachments/assets/ae086090-0bad-4992-b08e-0edc259fcf53" />


---

### Những thứ mình tự học thêm

- **PowerBI:** Sau khi nhận ra là tableau quá đắt và lạc quẻ cho các công ty Châu Á, mình bắt đầu nạp thêm kiến thức về PowerBI, Dax function
- **IT infrastructure:** Phần này thì mình học khoá IT Support của Google và Computer Science for Business Professional của Harvard. Nghe thì có vẻ không liên quan nhưng nó đã giúp mình rất nhiều trong việc học và giao tiếp với các tech stack của data engineer.
- **AWS S3, Lambda:** Tự học để viết API, dùng API đi crawl data
- **Selenium:** Tất nhiên là để crawl data từ những nơi không có API rồi.
- **Những món của Data Engineer:** AWS Redshift, Athena, Glue, Azure Synapse,… hay các công nghệ như OLAP, các tool ETL: Công ty đào tạo hoặc mình vác máy qua nhờ các bạn DE chỉ cho. Tại vì nếu dùng các hệ thống như Redshift thì sẽ phải lên đây tính sẵn các Measures rồi đưa về BI tools. Nếu bạn hiểu về hạ tầng mạng thì tiếp thu những thứ này sẽ nhanh hơn tí

---

### Những thứ mình đang học:

- **DP-100:** Designing and Implementing a Data Science Solution on Azure
- **TensorFlow + Keras** (đang học trên Datacamp và Google)

---

## Nếu được quay lại 5 tháng trước thì mình sẽ học Data Analyst theo lộ trình này

1. Học chứng chỉ của Google để đặt nền tảng kiến thước trước => Google Data Analytics Professional Certificate
2. Học track Data Analyst của DataCamp, tập trung SQl và PowerBI => lấy chứng chỉ DataCamp Data Analyst Associate => Bắt đầu đi Apply intern hoặc các job thiên về reporting
3. Học nâng cao Python, EDA, hypothesis testing,… => lấy chứng chỉ Datacamp Data Analyst Professional
4. Học các công cụ của Azure, AWS

---

## Chọn project để làm portfolio thế nào?

Theo mình một project thành công nên có đủ các skill cần dùng trong công việc thực tế

- Tìm data source
- Dùng API để lấy data, hoặc scrape data về (Selenium hoặc scrappy,…), vì thực tế ngoài đời toàn làm thế.
- Nếu có sẵn một cái SQL server để login vào thực hành thì quá tốt.
- Phân tích Data, EDA, Validation
- Model fitting + Evaluation (cho các data Science project)
- Visualization
- Insight + recommendations
- Nếu project có thể tự động update, refresh data thì càng tốt

Mình thì chia nhỏ các yêu cầu này ra thành các project khác nhau.

Mỗi loại data thường có 1 vấn đề riêng mà chúng ta có thể tận dụng 1 công nghệ để giải quyết, show-off kỹ năng.  
Nếu bạn dùng data có sẵn rồi Visualize bằng PowerBI hoặc Tableau cũng được, dùng SQL pull data về cũng được.  
Tuỳ công ty mà họ sẽ thấy kỹ năng của bạn phù hợp hay không để tuyển  
Đừng dùng các dataset quá cũ và nổi tiếng như Titanic nữa. Nó không thực tế và data đó cũng quá đẹp.

---

## Những thủ thuật để việc học tốt hơn:

- Bí cái gì thì cứ lên Google mà tìm đọc lý thuyết.
- Microsoft, Google, Amazon Web Service có đầy đủ các tài liệu hướng dẫn, giải thích rất hay về Data, Machine learning. Họ cung cấp hoàn toàn miễn phí.
- Bí code thì cứ StackOverflow mà chiến
- Một trong những nơi học tốt nhất, đó là đi phỏng vấn. Khi đi phỏng vấn, người ta sẽ gởi cho bạn các bài screening test, bạn sẽ có những cái nhìn rõ hơn về việc người ta tét cái gì và bạn đáp ứng được gì.
- Nếu đọc lý thuyết mà không hiểu thì lên Youtube coi các chuyên gia giải thích kỹ hơn. Có rất nhiều kênh YouTube giải thích 5 phút bằng mình tự đi tìm hiểu 50 phút.

---

## Các công cụ visualize code

<img width="1600" height="999" alt="6165595_Screen_Shot_2022-10-15_at_14 43 06" src="https://github.com/user-attachments/assets/bc3c4f83-93fb-466a-a012-81c8319dad6f" />

Computer Science Circle của Waterloo University: https://cscircles.cemc.uwaterloo.ca có các tool visualize code rất hay

---

## Những nơi bạn có thể luyện SQL:

- Hackerrank
- Leetcode
- DataLemur

---

## Những thắc mắc thường gặp khi học Data Analyst

- **Bắt đầu từ đâu?** ==> hãy tin mình, học khoá học của Google trước đi
- **Quan trọng nhất là phải học Python???** ==> Python phổ biến vì nó làm được nhiều thứ, nhưng trong DA nó chưa chắc là thứ quan trọng nhất. Trong những công ty có tổ chức data hoàn chỉnh thì thường DA sẽ được tiếp cận với data ở Gold level, mọi thứ đã được các bạn Data Engineer clean và xử lý xong hết rồi (Cảm ơn các bạn DE rất nhiều 😁 ). Thứ quan trọng không kém mà một DA cần quan tâm là SQL. Bạn sẽ làm việc với SQL rất nhiều. Khi làm việc với các data lớn bạn sẽ phải dùng các tool SQL, ví dụ Spark SQL, AWS Redshift hay AWS Athena hay các SQL sever. Bạn phải lấy số liệu từ SQL rất nhiều. Các tool visualization cũng có cần SQL để lấy data về dựng chart.
- **Tableau > PowerBI????** ==> Đúng, nhưng mà sai. Mình là fan ruột của Tableau vì nó nhanh hơn, tiện lợi hơn, thông minh hơn. Tuy nhiên tiền phí bản quyền Tableau khá là đắt. Nên nếu bạn nào muốn làm Data ở Việt Nam thì cân nhắc học PowerBI vì các doanh nghiệp thường không muốn bỏ tiền ra để mua Tableau đâu. Lý do nữa là hạ tầng Microsoft Office 365 được dùng ở rất nhiều doanh nghiệp nên Microsoft PowerBI mặc định sẽ được sử dụng cho nó tiện và tiết kiệm
- **Học khoá học Google xong có đi làm được không?** ==> Không thể
- **Học Datacamp hay Dataquest.io** => Mình không biết, nhưng danh tiếng datacamp thì lớn hơn, phổ biến hơn
- **Trên Coursera, học khoá của Google hay IBM?** => Mình học audit khoá của IBM thì thấy khoá của Google cung cấp kiến thức nền tảng tốt hơn, khoá của IBM thì thực hành tốt hơn. Nhưng phần thực hành thì mình học trên Datacamp rồi nên mình không bỏ tiền ra lấy cert của IBM nữa.
- **Có cần làm website portfolio không?** ==> Có nhé. Nên có. Dùng các dịch vụ có sẵn như Wix hay WordPress.com cũng được. Tham khảo bài viết này: https://careerfoundry.com/en/blog/data-analytics/data-analytics-portfolio-examples/#claudia-ten-hoope
- **Đi học trung tâm có được không?** Mình không biết, tại vì mình tự học, không đi học trung tâm. Nhưng mình có tham khảo qua khoá học của vài trung tâm thấy cũng sát thực tế so với những gì mình dùng trong công việc. Nhưng có trung tâm thì bánh vẽ lắm. Giáo trình dạy Data Analyst từ còn số 0 mà vẽ qua hướng Machine learning rất nặng. Chả biết để làm gì.

---

## Học như vậy rồi có đi làm được không?

Câu trả lời **ĐƯỢC, thậm chí là làm Tốt. Nhưng nó còn tuỳ.**

- Tuỳ bạn học vẹt hay bạn học thật
- Tuỳ công việc bạn apply phức tạp đến cỡ nào
- Tuỳ năng lực tư duy của mỗi người.
- Tuỳ kinh nghiệm làm việc trước đây
- Tuỳ nền tảng kiến thức của mỗi người.

---

Lần trước mình có viết là mình học data trong 5 tháng là xin việc thành công. Nhiều bạn bảo là mình chém gió, làm sao mà học nhanh vậy được. Nên bài viết này cũng sẽ giải thích cho sự thắc mắc đó, hy vọng anh em vui vẻ đừng quạu quọ làm gì (mau già lắm).

Mình viết bài để chia sẻ và giúp đỡ những người đi sau khỏi gặp vấn đề như mình. Mấy anh Senior nếu có thấy gì không đồng tình thì hãy bớt tí thời gian viết bài chia sẻ và giúp đỡ những người mới, cho đàn em đi sau 😁

Ai thắc mắc gì cứ comment ở dưới nha. Mình biết thì mình trả lời. Không biết thì mình đi hỏi hộ cho 😀

_Last Update: December 1, 2024_
