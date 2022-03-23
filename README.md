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
