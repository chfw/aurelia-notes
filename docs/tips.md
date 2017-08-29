# Tips for angular 1 users

## call `$injector` as a function

With angular 1, you can use `$injector` function to do custom depdency injection. With
Aurelia, I am struggled and found a similar function:

```
import {Your_Class} from 'your_plugin';

... // any where there is aurelia : Aurelia

const single_instance = aurelia.container.get(Your_Class);
...
```

