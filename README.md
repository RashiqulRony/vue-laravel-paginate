# vue laravel paginate 
_**this package use only laravel api purpose**_


### Install Package
```
npm install vue-laravel-paginate
```

### Import Package
```javascript
import Paginate from "vue-laravel-paginate";
```

### Implementation example
```javascript
components: {
  Paginate
},

data() {
    return {
      data: []
    }
},

mounted() {
  this.getData()
},

methods:{
    getData(page = 1) {
        axios.get('your-laravel-api').then((response) => {
          this.data = response.data
        }).catch((error) => {
          console.log(error);
        });
    },
}
```

### Implementation html example
```vue
  <Paginate v-on:changepage="getData($event)" 
            :from="data.from" 
            :to="data.to" 
            :total="data.total" 
            :links="data.links"
            :currentPage="data.current_page"/>
```
### Required attribute:
```
1. v-on:changepage="getData($event)"
2. :links="data.links"
3. :currentPage="data.current_page"
```

### Laravel API:
```php
return User::paginate(25);
```


###  Author Info
**Name:** Rashiqul Rony <br>
**Github**: https://github.com/RashiqulRony
