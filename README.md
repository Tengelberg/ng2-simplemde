[![Build Status](https://img.shields.io/travis/doxiaodong/ng2-simplemde.svg?style=flat-square)](https://travis-ci.org/doxiaodong/ng2-simplemde)
[![Downloads](https://img.shields.io/npm/dt/ng2-simplemde.svg?style=flat-square)](https://www.npmjs.com/package/ng2-simplemde)
[![Versions](https://img.shields.io/npm/v/ng2-simplemde.svg?style=flat-square)]()
[![License](https://img.shields.io/npm/l/ng2-simplemde.svg?style=flat-square)]()

# simplemde-markdown-editor with Angular

# demo
  [https://doxiaodong.github.io/ng2-simplemde](https://doxiaodong.github.io/ng2-simplemde)

# Usage

* install `npm i ng2-simplemde --save`

```typescript
import { NgModule } from '@angular/core'
import { SimplemdeModule, SIMPLEMDE_CONFIG } from 'ng2-simplemde'
@NgModule({
  imports: [
    SimplemdeModule.forRoot({
      provide: SIMPLEMDE_CONFIG,
      // config options 1
      useValue: $options1
    })
  ],
  bootstrap: [AppComponent]
})
export class AppModule { }
```

```html
<!-- config options 2 -->
<simplemde [(ngModel)]="value" [options]="$options2"></simplemde>
```

> 1. The final options is `{...$options1, ...$options2}`, `Object.assign({}, $options1, $options2)`
> 2. The `element` option is not useful
