# Angular Learn

## Setup and Installation

1. Install Node.js

```
curl -sL https://deb.nodesource.com/setup_12.x | sudo -E bash -
sudo apt-get install -y nodejs
```

2. Update NPM

```
sudo npm install npm@latest -g
```

3. Install the Angular CLI

```
sudo npm install -g @angular/cli
```

4. Create a new project/workspace

```
ng new example-app
```

## Angular Command

- Serving the page

```
ng serve
```

- Generate a component

```
ng generate component my-component-name

or

ng g c my-component-name
```

- Install a package

```
npm install <package-name>
eg: npm install bootstrap
```

## Angular Data Binding

1. Interpolation / Angular Expression

card.component.ts

```js
export class CardComponent implements OnInit {

  //variable
  public typeName:string = "Company"

  constructor() { }

  ngOnInit(): void {
  }

}
```

card.component.html

```html
<div class="card shadow-lg">
                    <img src="https://cdn.corporatefinanceinstitute.com/assets/affiliated-companies-1024x614.jpeg" alt="" class="image-fluid">
                    <div class="card-body">
                        <h3>{{ typeName }}</h3>
                        <p>Lorem ipsum dolor sit amet consectetur adipisicing elit. Alias iste repudiandae quaerat, odit reiciendis sapiente culpa? Ipsam obcaecati voluptatem ab.</p>
                        <button class="btn btn-danger">Book Now</button>
                    </div>
                </div>
```



2. **Prop Binding**



card.component.ts

```js
export class CardComponent implements OnInit {

  //variable
  public typeName:string = "Company";
  public compImage:string = "https://cdn.corporatefinanceinstitute.com/assets/affiliated-companies-1024x614.jpeg"

  constructor() { }

  ngOnInit(): void {
  }
  
}
```

card.component.html

```html
<img [src]="compImage" alt="" class="image-fluid">
```



3. **Event Binding**



card.component.ts

```js
public counter:number = 0;


public incrementNumber():void {
    this.counter++;
  }

  public decrementNumber():void {
    this.counter--;
  }
```



card.component.html

```html
<p class="h4 mt-5">Counter: {{ counter }}</p>
<button (click)="incrementNumber()" class="mt-3 m-3 btn btn-success">Increment</button>
<button (click)="decrementNumber()" class="mt-3 m-3 btn btn-danger">Decrement</button>
```
