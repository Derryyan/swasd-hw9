# 系统分析与设计第九周作业

## 1.使用类图，分别对 Asg_RH 文档中 Make Reservation 用例以及 Payment 用例开展领域建模。然后，根据上述模型，给出建议的数据表以及主要字段，特别是主键和外键

 - Make Reservation

    ![1][1]
        
    Hotel (ID/Key, LocationID/FKey, Name, Address, Brief-intro, isFavourites, isLowestPrice, isHigestStarRating, isAlphabetical)) 
    
    Location (LocationID/Key, Name, isFavourite)
    
    Room (ID/Key, HotelID/FKey, Type, Date, isAvailable, isReserved, Price)
    
    ReservationItem (ID/Key, ReservationID/FKey, RoomID/Fkey, AdultsNum, ChildrenNum,CheckInDate, NumberofNights)
    
    Reservation (ID/Key, TravelerID/FKey, HotelID/FKey, CheckInDate, NumberofNights)
    
    Traveler (ID/Key, Name, EmailAddress)    
    
 - Payment
    
    ![2][2]
   
    Customer (CustomerID/Key,Name,Password,EmailAddress)
    
    CreditCard (ID/Key,CustomerID/FKey,Type)
    
    CreditCardDescription (ID/Key,Password,OwnerID)
    
    Payment (CustomerID/Key,ReservationID/FKey,Detail,Price)

## 2.使用 UML State Model，对每个订单对象生命周期建模

 ![3][3]





 


  [1]: https://github.com/Derryyan/swasd-hw9/raw/master/1.png
  [2]: https://github.com/Derryyan/swasd-hw9/raw/master/2.png
  [3]: https://github.com/Derryyan/swasd-hw9/raw/master/3.png
