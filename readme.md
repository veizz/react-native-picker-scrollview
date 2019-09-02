## react-native-picker-scrollview

a pure js picker, each option item customizable

![example](./res/demo.gif)


### usage

```shell
npm install react-native-picker-scrollview --save
```

```jsx
import React, {Component} from 'react';
import ScrollPicker from 'react-native-picker-scrollview';

export default class SimpleExample extends Component {

    render() {
        return(
            <ScrollPicker
                ref={(sp) => {this.sp = sp}}

                dataSource={[
                    'a',
                    'b',
                    'c',
                    'd',
                ]}
                selectedIndex={0}
                itemHeight={50}
                wrapperHeight={250}
				wrapperColor={'#ffffff'}
                highlightColor={'#d8d8d8'}
                renderItem={(data, index, isSelected) => {
                    return(
                        <View>
                            <Text >{data}</Text>
                        </View>
                    )
                }}
                onValueChange={(data, selectedIndex) => {
                    //
                }}
            />
        )
    }


    //
    someOtherFunc(){
        this.sp.scrollToIndex(2);   // select 'c'
        let selectedValue = this.sp.getSelected();  // returns 'c'
    }
}
```
