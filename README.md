# NumberStepper [![](https://jitpack.io/v/czy1121/numberstepper.svg)](https://jitpack.io/#czy1121/numberstepper)


![screenshot](screenshot.png)

## Gradle

``` groovy
repositories { 
    maven { url "https://jitpack.io" }
} 
dependencies {
    compile 'com.github.czy1121:numberstepper:1.2.0'
}
```
    
## Usage
    
**XML**

``` xml
<ezy.ui.view.NumberStepper
    android:id="@+id/ns"
    style="@style/NumberStepper"
    app:nsMaxValue="100"
    app:nsMinValue="1"
    app:nsStep="1"
    app:nsValue="5"
    />
```

**Java**

``` java
nsValue = (NumberStepper) findViewById(R.id.ns);
nsValue.setOnValueChangedListener(new NumberStepper.OnValueChangedListener() {
    @Override
    public void onValueChanged(NumberStepper view, int value) {
        txtValue.setText("" + value);
    }
});
// init(step, min, max, value)
nsValue.init(5, -10, 100, 8); 
```
 