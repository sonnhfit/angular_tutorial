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

### Show component 

Để hiển thị bạn có thể sử dụng cú pháp như trong django hay flask trong template 

dùng ký hiệu ```{{ hero }}```

#### Format với Pipe 

Angular hỗ trợ rất nhiều kiểu để bạn có thể tùy chỉnh cách hiển thị để sử dụng pipe bạn làm như sau

```html
<h2>{{hero.name | uppercase }} Details </h2>

```
### Binding 

#### Two-way binding 

sử dụng ngModel để binding dữ liệu

```html

<div>
  <label>name:
    <input [(ngModel)]="hero.name" placeholder="name"/>
  </label>
</div>

```

Lưu ý cần phải import thư viện sau 

```angularjs
import { FormsModule } from '@angular/forms';
```

### Hiển thị danh sách 

```html

<h2>My Heroes</h2>
<ul class="heroes">
  <li *ngFor="let hero of heroes">
    <span class="badge">{{hero.id}}</span> {{hero.name}}
  </li>
</ul>

```

sử dụng *ngFor để in ra danh sách

### Sử lý sự kiện onclick 

để thêm sự kiện onclick vào một element chúng ta làm như sau 

```html
<li *ngFor="let hero of heroes" (click)="onSelect(hero)">
```

