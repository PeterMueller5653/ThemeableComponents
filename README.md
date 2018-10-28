[![](https://jitpack.io/v/DerTyp7214/ThemeableComponents.svg)](https://jitpack.io/#DerTyp7214/ThemeableComponents)

# ThemeableComponents

## To import the lib


### 1. Add it in your root build.gradle at the end of repositories
```gradle
allprojects {
    repositories {
        ...
        maven { url 'https://jitpack.io' }
    }
}
```

### 2. Add the dependency:
```gralde
dependencies {
    implementation 'com.github.DerTyp7214:ThemeableComponents:<LATEST_VERSION>'
}
```

## Usage

### List of ThemeableComponents:

ThemeableComponents | Original
------------------------------------------------------------- | --
`com.dertyp7214.themeablecomponents.components.ThemeableButton` | MaterialButton
`com.dertyp7214.themeablecomponents.components.ThemeableCheckBox` | AppCompatCheckBox 
`com.dertyp7214.themeablecomponents.components.ThemeableEditText` | TextInputEditText 
`com.dertyp7214.themeablecomponents.components.ThemeableFloatingActionButton` | FloatingActionButton 
`com.dertyp7214.themeablecomponents.components.ThemeableProgressBar` | ProgressBar 
`com.dertyp7214.themeablecomponents.components.ThemeableRadioButton` | AppCompatRadioButton 
`com.dertyp7214.themeablecomponents.components.ThemeableSeekBar` | AppCompatSeekBar 
`com.dertyp7214.themeablecomponents.components.ThemeableSwitch` | Switch 
`com.dertyp7214.themeablecomponents.components.ThemeableToggleButton` | ToggleButton
`com.dertyp7214.themeablecomponents.components.ThemeableToolbar` | Toolbar 
`com.dertyp7214.themeablecomponents.components.ThemeableView` | View 

use them like the normal ones.

In your Activity you can get the ThemeManager: `ThemeManager.getInstance(this)`

### Functions:

Function | Description
-- | --
`List<Component> : themeManager.getComponents()` | gets all Components
`List<Component> : themeManager.getComponents(this)` | gets all Components from this Activity
`List<Component> : themeManager.filterComponents(List<Component>, ThemeManager.Component.TYPE)` | filters the Components by Type


### ChangeColors:

Function | Description
-- | --
`themeManager.changeAccentColor(color)` | changes the color of all accent components
`themeManager.changeAccentColor(color, animated)` | changes the color animated of all accent components
`themeManager.changePrimaryColor(color)` | changes the color of all primary components
`themeManager.changePrimaryColor(color, animated)` | changes the color animated of all primary components
`themeManager.changePrimaryColor(activity, color, statusBar, navigationBar)` | changes the color of all primary components and the navigation, status-bar
`themeManager.changePrimaryColor(activity, color, statusBar, navigationBar, animated)` | changes the color animated of all primary components and the navigation, status-bar


### ColorPicker

```Java
ColorPicker colorPicker = new ColorPicker(activity);
colorPicker.setColor(color);
colorPicker.setAnimationTime(duration);
colorPicker.setListener(new ColorPicker.Listener() {
    @Override
    public void color(int color) {

    }

    @Override
    public void update(int color) {

    }

    @Override
    public void cancel() {

    }
});
colorPicker.show();
colorPicker.setDarkMode(darkmode);
```
