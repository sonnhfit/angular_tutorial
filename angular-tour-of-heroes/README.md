# Chạy project 

```angular2
ng serve --open
```

# Nội dung chính 

* Khởi tạo project bằng lệnh 

```angularjs
ng new <project name>
```

## Component 

* khởi tạo component 

để khởi tạo compoent bạn sử dụng lệnh sau 
```angularjs
ng generate component <ten component>
```

- selector 
định nghĩa tag  cách mà bạn sẽ gọi khi CSS 
- templateUrl 
Vị trí của component template file 
- style Urls 
Lơi chứa các css riêng của component 

### Thuộc tính của component 
Bạn có thể khai báo thuộc tính của một component, thuộc tính có thể là một thuộc tính như thuộc tính của l
ớp hoăc có thể là một đối tượng ví dụ như thế này:

```angularjs
hero = 'Windstorm';
```

hoặc như thế này 

```angularjs
hero: Hero = {
    id: 1,
    name: 'Windstorm'
  };
```
