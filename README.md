# პროექტის მიმოხილვა – Walmart Recruiting: Store Sales Forecasting


## მონაცემების აღწერა

  მონაცემები შეიცავს შემდეგ სვეტებს:
  
  Store – მაღაზიის უნიკალური იდენტიფიკატორი
      
  Dept – დეპარტამენტის იდენტიფიკატორი
  
  Date – კვირის პირველი დღე (დროითი ღერძი)
  
  Weekly_Sales – იმ კვირაში გაყიდული პროდუქციის თანხა (ჩვენი სამიზნე ცვლადი)
  
  IsHoliday – აღნიშნული კვირა მოიცავს თუ არა დღესასწაულს
  
  დამატებით მოცემულია:
  
  features.csv – გარეგანი ფაქტორები, როგორიცაა CPI, ბენზინის ფასი, უმუშევრობის დონე და ა.შ.
  
  stores.csv – მაღაზიების ტიპი და ზომა

## მონაცემების ანალიზი 

  ### cleaning
  პროექტის საწყის ეტაპზე მოხდა მოცემული სამივე მონაცემის ფაილის (train.csv, features.csv, stores.csv) გაერთიანება Store და Date სვეტების მიხედვით.
  Weekly_Sales ცვლადში აღმოჩენილი უარყოფითი ან ნულოვანი მნიშვნელობები წარმოადგენდა მხოლოდ 0.3%-ს. ისინი იქნა ამოღებული.
  Markdown სვეტებში იყო ბევრი NaN მნიშვნელობა. ისინი ჩავანაცვლეთ 0-ით.
  ### თარიღის დამუშავება
  -- Date ველი გარდაიქმნა datetime ფორმატში, რის შემდეგაც შეიქმნა ახალი სვეტები:
            year,month,week.
  -- ასევე განვათავსეთ ოთხი მნიშვნელოვანი დღესასწაული ცალკე ბულიან სვეტებად, რადგან გვინდოდა გვენახა , როგორ იყო დამოკიდებული weekly_sales მათთან:
            Thanksgiving,Christmas,Super_Bowl,Labor_Day


 
  ![image](https://github.com/user-attachments/assets/b6a1d80e-30d2-4a18-86a5-6f4a990184c6)

  
  ![image](https://github.com/user-attachments/assets/0c2b497f-999e-44c8-abdc-cf68d596c057)


  ![image](https://github.com/user-attachments/assets/219e6d87-26f2-496f-b189-13029ed87c5c)


  ![image](https://github.com/user-attachments/assets/363bf5f2-fc18-4521-8b68-f74acce58a48)


  ![image](https://github.com/user-attachments/assets/e5ad498a-f0db-4a34-893e-9be6df769040)



  ჩანს , რომ Labor Day და Christmas ძალიან არ ცვლის გაყიდვებს. ყველაზე მეტად მასზე ახდენს ზემოქმედებას Thanksgiving.


  ## დეპარტამენტები და მაღაზიები
  
  მონაცემები მოიცავს 45 მაღაზიას და 81 დეპარტამენტს – თუმცა ყველა დეპარტამენტი არ არის ხელმისაწვდომი ყველა მაღაზიაში.
  ყველაზე მაღალი საშუალო გაყიდვები ჰქონდა დეპარტამენტს 92, თუმცა ყველაზე მაღალი ინდივიდუალური გაყიდვები იყო დეპარტამენტი 72-ში, ძირითადად Thanksgiving-ის კვირაში.

  მაღაზიებს აქვთ ტიპები A, B, C — ტიპი A უდიდესია ზომით (>150,000), და მას აქვს ყველაზე მაღალი საშუალო გაყიდვები.

  ყველაზე მაღალი გაყიდვები დაფიქსირდა Thanksgiving-ის, Christmas-ის და Black Friday-ის კვირებში (კვირები 47–51).

  
  
  ![image](https://github.com/user-attachments/assets/578b19a8-659d-432f-862b-61ae0503caff)


  ![image](https://github.com/user-attachments/assets/5da5436a-f2fd-4149-8cf5-aee4382f5089)


  ![image](https://github.com/user-attachments/assets/16f07a85-c2ca-475d-bbee-dca926a10da0)


  ![image](https://github.com/user-attachments/assets/43305902-de05-446a-bd66-bd0ac2328d52)


  ![image](https://github.com/user-attachments/assets/a1708504-c633-43b8-a3ba-8f1f2f737c34)


  ქვედა გფაფი აჩვენებს გაყიდვებს წლების მიხედვით.

  

  ![image](https://github.com/user-attachments/assets/603177ee-071d-4e42-a131-919f8bc016fb)

  

  კვირების მიხედვით:


  ![image](https://github.com/user-attachments/assets/730193dc-8cbb-40bb-b3ef-989a510be193)



   CPI, Fuel Price, Unemployment, Temperature არ აჩვენებს გამოკვეთილ კორელაციას Weekly_Sales-თან.



   ![image](https://github.com/user-attachments/assets/116c2ee3-530f-4b9b-8b44-e9f84e6ad605)



   ![image](https://github.com/user-attachments/assets/22c91452-e4fb-44ea-84f8-69c5fb72dfde)



   ![image](https://github.com/user-attachments/assets/a9d92048-8f56-49bf-9350-b2f6eca4185a)



   ![image](https://github.com/user-attachments/assets/c2c4b0ed-8aa4-4d05-8b5e-f9d612be6bf6)









  
  

  


 






  
