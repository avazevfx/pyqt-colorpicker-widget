# PyQt5 Color Picker

Simple Color Picker Widget created with PyQt5 to easily get color input from the user.

![colorpicker_widget](https://user-images.githubusercontent.com/71983360/95210784-233feb80-07ec-11eb-94fb-3fb1efc48ae3.png)


## Usage

1. To use the Color Picker Widget in a PyQt5 project make sure you have the `PyQt5` library:

   ```
   pip install PyQt5
   ```

   then add the `colorpicker` folder into your project folder and import `ColorPicker`

   ```python
   from colorpicker import ColorPicker
   ```

2. To add the widget to your app, create a `360x200` placeholder widget in your ui and add the colorpicker to it:

   ```python
   colorpicker = ColorPicker(my_placeholder)
   ```

   and then run `getRGB`/`getHSV`/`getHex` method to get the currently selected color:

   ```python
   current_color = colorpicker.getRGB()
   ```


* `getRGB` returns a rgb tuple with values from 0-255,
* `getHSV` returns a hsv tuple with values from 0-100,
* `getHex` returns a string without hashtag.

* You can customize the ranges easily:

   ```python
   hsv = colorpicker.getHSV(360,1)  # hue in degrees, saturation & value from 0 to 1
   rgb = colorpicker.getRGB(100)    # rgb in percent
   hex = colorpicker.getHex(True)   # use hashtag in string
   ```

* Use ColorPicker's `colorChanged` signal to update directly when the user changes the color:

  ```python
  colorpicker.colorChanged.connect(my_function)

  def my_function():
    print(colorpicker.getColor())
  ```

* For an example with a bigger application based on a main class, look at the `example.py` file.
