# Django-Post-Sharing

A simple web application built with Django that allows users to share and view posts. Users can register, log in, create posts, and view posts shared by others.

---

## Features
- **User Authentication**: Register, log in, and log out functionality.
- **Create Posts**: Authenticated users can create new posts.
- **View Posts**: All users can view a list of shared posts.
- **Admin Panel**: Admins can manage users and posts via Django's built-in admin interface.

---

## Tech Stack
- **Backend**: Django (Python)
- **Frontend**: HTML, CSS, Django Templates
- **Database**: SQLite (default Django database)
- **Tools**: Django ORM, Django Admin Panel, Django Forms

---

## Screenshots 
![image](https://github.com/user-attachments/assets/cbe4df4f-e4b1-4d48-aa36-b0941de42dba)
![image](https://github.com/user-attachments/assets/73068c1a-3c85-44c2-b83a-2aa9b4849ccc)
![image](https://github.com/user-attachments/assets/37ffc011-f961-4c45-9ed3-12294f3ca7ff)
![image](https://github.com/user-attachments/assets/b3b45008-adfa-462f-ae44-2e33f977dc8c)
![image](https://github.com/user-attachments/assets/ee993cd8-6785-4a47-af53-79f41d2d3a75)
*The Login and Register buttons are visible when no user is logged in*
![image](https://github.com/user-attachments/assets/8b97de64-e2c6-4b89-8a13-2b97534f2657)
*Register page*
![image](https://github.com/user-attachments/assets/0f529363-2f8b-4e0e-9cf3-0e5696d232ce)
*Login Page*











---

## Models
 Post model
 ```
class Post(models.Model):
    title = models.CharField(max_length=75)
    body = models.TextField()
    slug = models.SlugField()
    date = models.DateTimeField(auto_now_add=True)
    banner = models.ImageField(default="monkey.jpeg", blank = True)
    author = models.ForeignKey(User, on_delete=models.CASCADE, default=None)

```
## References
[Dave Gray](https://www.youtube.com/watch?v=qcJZN1pvG6A&list=PL0Zuz27SZ-6NamGNr7dEqzNFEcZ_FAUVX&ab_channel=DaveGray) <br>
[Django Documentation](https://docs.djangoproject.com/en/5.1/)
