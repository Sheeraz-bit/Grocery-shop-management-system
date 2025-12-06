# Grocery-shop-management-system

## Directory Structures
### Backend
<pre>
./
└─ src/main/java/com/example/Grocery/Management/System/
   ├─ login/
   │  ├─ user.java
   │  ├─ user_repository.java
   │  ├─ user_services.java
   │  ├─ user_controller.java
   │
   ├─ shop/
   │  ├─ shop.java
   │  ├─ shop_repository.java
   │  ├─ shop_services.java
   │  ├─ shop_controller.java
   │
   ├─ order/
      ├─ order.java
      ├─ order_repository.java
      ├─ order_services.java
      ├─ order_controller.java
</pre> 
### Frontend
<pre>
./
└─ src/main/resources/templates/
   ├─ login/
   │
   ├─ staff dashboard/
   │  ├─ shop/
   │  ├─ order/
   │  ├─ customer/
   │
   ├─ admin dashboard/
      ├─ shop management/
      ├─ customer/
      ├─ order/
</pre>

---

## Database guide line
### step 1 - Install & start MySql
- Install MySQL (Server + Workbench) or use XAMPP / WAMP / etc.
- Make sure the MySQL service is running.

---

### step 2 - Open MySQL client
- Command Line
```cmd
mysql -u root -p
enter password-> 
```

---

### step 3 - Setup database
<a href="database_setup.md">Use this guide to setup database</a>

---
