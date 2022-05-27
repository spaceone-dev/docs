---
title: "Coding Convention"
linkTitle: "Coding Convention"
weight: 3
date: 2022-05-27
description: >
    Frontend Coding Convention
no_list: true
---


프론트엔드 코딩 컨벤션에 대한 문서입니다.
[Console](https://github.com/spaceone-dev/console), 
[Design System](https://github.com/spaceone-dev/spaceone-design-system),
[Core Lib](https://github.com/spaceone-dev/console-core-lib)


## Javascript - ECMAScript 2018(ES9)

| Item     | Category                   | Rule                 | Example                                      |
|----------|----------------------------|----------------------|----------------------------------------------|
| Class    |                            | PascalCase           | ```class myClass {}```                       |
| Function |                            | camelCase            | ```const myFunction = () => {}```            |
| Variable | Readonly const <br /> Enum | SCREAMING_SNAKE_CASE | ```const READONLY_CONST <br /> MY_ENUM {}``` |
|          | Others                     | camelCase            | ```myVariable```                             |


## Typescript

| Item      | Category           | Rule       | Example                        |
|-----------|--------------------|------------|--------------------------------|
| Type      |                    | PascalCase | ```type MyType = type;```      |
| Interface |                    | PascalCase | ```interface MyInterface {}``` |


## File / Directory / URL   

| Item                 | Repo          | Category                        | Rule                                                                             | Example                                                                                                                          |
|----------------------|---------------|---------------------------------|----------------------------------------------------------------------------------|----------------------------------------------------------------------------------------------------------------------------------|
| Files                | Console       | Vue Components                  | PascalCase                                                                       | MyComponent.vue                                                                                                                  |
|                      |               | Pages                           | PascalCase <br /> with suffix 'Page'                                             | MyConsolePage.vue                                                                                                                |
|                      | Design System | Components <br /> Related Files | PascalCase <br /> with prefix 'P' (means 'Prime') <br /> with its component name | PMyDSComponent.vue <br /> PMyDSComponent.mdx <br /> PMyDSComponent.stories <br /> PMyDSComponent.scss <br /> PMyDSComponent.pcss |
|                      |               | Type Related Files              | kebab-case <br /> with suffix '-type'                                            | type.ts <br /> schema-type.ts                                                                                                    |
| Other Files          | Common        |                                 | kebeb-case                                                                       | my-config.ts                                                                                                                     |
| Directory <br /> URL | Common        |                                 | kebab-case                                                                       | /my-directory <br /> /my-url/                                                                                                    |


## Code

| Item  | Repo          | Category           | Rule                                                                                                                                                                                                                                 | Example                                                                         |
|-------|---------------|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|---------------------------------------------------------------------------------|
| Event | Common        | Name               | Verb Root <br /> If duplicated or needed -ed / -ing is allowed                                                                                                                                                                       | update <br /> update, updated                                                   |
|       |               | Two-way Binding    | If the event needs two-way biding, emit 'update:xxx'                                                                                                                                                                                 | ```$emit('update:code', code)```                                                |
|       |               | Arguments          | ```$event``` as the last argument                                                                                                                                                                                                    | ```$emit(foo, bar, $event)```                                                   |
| Code  | Common        | Handler Name       | Clear word with prefix 'handle'                                                                                                                                                                                                      | ```const handleOnClick = () => {}```                                            |
|       |               | Component Name     | PascalCase at script files <br /> kebab-case at template                                                                                                                                                                             | ```<my-component />``` <br /> ```import MyComponent from @```                   |
|       |               | Composition API    | 1. Do not declare objects,variables inside ```return``` <br /> 2. The name of ```reactive``` variable should be ```state or xxxState (if needed)``` <br /> 3. Using variable inside ```setup()``` is recommended as ```reactive```   | 1. ```const a = 1; return { a }``` <br /> 2,3. ```const state = reactive({})``` |
|       | Console       | Page script, style | 1. ```<script>``` lang should be **'ts'** <br /> 2. ```<style>``` lang should be **'postcss'** and **'scoped'**                                                                                                                      | 1. ```<script lang="ts">```<br /> 2. ```<style lang="postcss" scoped>```        |
|       | Design System | Page script, style | 1. ```<script>``` lang should be **'ts'** <br /> 2. ```<style>``` lang should be **'postcss'** ***BUT NO*** **'scoped'**                                                                                                             | 1. ```<script lang="ts">``` <br /> ```<style lang="postcss">```                 |
|       |               | Storybook Title    | Directories + component name(PascalCase) with dash                                                                                                                                                                                   | ```{ title: 'atoms/buttons/MyButton' ... }```                                   |
|       |               | Root Class Name    | Component name should be written on root element's class with kebab-case                                                                                                                                                             | ```<fragment class="p-my-button">```                                            |
|       | Core Lib      | Description        | Description of each function should be written, by JS Doc                                                                                                                                                                            | ```/** @@function @name @description *@param descriptions **/```                |


## Additional Rules
1. Array 에서 변수명 지정은 복수형보다 List 접미사를 지향합니다. 
```typescript
const policies: Array<string>; (X)
const plicyList: Array<string>; (O)
```

2. ```enum``` 혹은 ```Object.freeze()``` 대신 ```as const``` 를 사용합니다.
```typescript
const NOTIFICATION_UNIT = {
  PERCENT: 'PERCENT',
  ACTUAL_COST: 'ACTUAL_COST',
} as const;
```

3. API 응답 결과값에 대한 interface 명은 xxxModel 이라고 명명합니다.
```typescript
interface CostQuerySetModel {};
```

4. init 할 때 실행할 함수는 setup 함수 최하단에 위치시키는 것을 지향합니다.

    async 인 경우에는 즉시실행함수로 작성합니다.
```typescript
(async () => {
	await listCostQuerySet();
})();

return { ...toRefs(), ... }
```


## Test Code

console과 Design System 에서는 공통적으로 [vue test utils](https://v1.test-utils.vuejs.org/) 를 사용합니다.

파일명: ``` __test__/<대상 파일 명>.test.ts```

테스트코드 템플릿

```typescript
import { mount, createLocalVue } from '@vue/test-utils';
import CompositionApi, { defineComponent } from '@vue/composition-api';

const localVue = createLocalVue();
localVue.use(CompositionApi);

describe('', () => {
    const mockComponent = defineComponent({
        template: `
            <div>
            </div>
        `,
        setup() {
            return {};
        },

    });

    const wrapper = mount(mockComponent, { localVue });

    it('', () => {
        expect(wrapper.exists()).toBe(true);
    });
});
```

## Lint

- [ESLint](https://github.com/spaceone-dev/console/blob/master/.eslintrc.js)
- [StyleLint](https://github.com/spaceone-dev/console/blob/master/stylelint.config.js)

## References

- [Google JavaScript Style Guide](https://google.github.io/styleguide/jsguide.html#features-classes)
- [Airbnb JavaScript Style Guide](https://github.com/airbnb/javascript)
- [Vue.js Official Style Guide](https://kr.vuejs.org/v2/style-guide/)
