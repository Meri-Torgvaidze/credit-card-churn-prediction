# credit-card-churn-prediction

Predicting bank customer churn and identifying key driving factors using machine learning



Bank Credit Card Churn Prediction

პროექტი აანალიზებს საბანკო კლიენტების ქცევით და დემოგრაფიულ

მონაცემებს და პროგნოზირებს გადინების რისკს. შედარებულია ოთხი

კლასიფიკაციის მოდელი: Logistic Regression, Decision Tree,

Random Forest და XGBoost. საუკეთესო შედეგი მიღებულია XGBoost-ით

(Accuracy: 96.8%, F1-Score: 90.1%).



პროექტის სტრუქტურა

bank-churn-prediction/

&#x09;data\_loading.ipynb

&#x09;exploratory\_data\_analysis.ipynb

&#x09;modeling.ipynb

&#x09;BankChurners.csv

&#x09;requirements.txt

&#x09;outputs/

&#x09;README.md



გაშვება

pip install -r requirements.txt

jupyter notebook

Notebook-ები უნდა გაეშვას თანმიმდევრობით:

1\. data\_loading.ipynb

2\. exploratory\_data\_analysis.ipynb

3\. modeling.ipynb



\## შედეგები



| მოდელი            | Accuracy | Precision | Recall | F1-Score |

|---------------------|----------|-----------|--------|----------|

| Logistic Regression | 82.7%    | 47.6%     | 76.9%  | 58.8%    |

| Decision Tree       | 91.9%    | 69.8%     | 87.7%  | 77.8%    |

| Random Forest       | 95.4%    | 84.5%     | 87.1%  | 85.8%    |

| XGBoost             | 96.8%    | 90.4%     | 89.9%  | 90.1%    |



\## ძირითადი მიგნებები

\- 16%-იანი class imbalance გამოსწორდა SMOTE-ის გამოყენებით

\- Total\_Trans\_Ct: ტრანზაქციების დაბალი სიხშირე churn-ის ყველაზე ძლიერი მაჩვენებელია

\- Total\_Trans\_Amt: დაბალი დახარჯული თანხა უკავშირდება გადინების მაღალ რისკს

\- Total\_Revolving\_Bal: დაბალი საბრუნავი ბალანსი მიუთითებს კლიენტის დაბალ ჩართულობაზე

\- Total\_Relationship\_Count: მეტი საბანკო პროდუქტის მომხმარებელი კლიენტები უფრო ლოიალურები არიან

\- Total\_Ct\_Chng\_Q4\_Q1: ტრანზაქციების სიხშირის შემცირება დროთა განმავლობაში გადინების მნიშვნელოვანი გამაფრთხილებელი სიგნალია

