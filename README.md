# PyQt5 Color Picker
Simple Color Picker Widget created with PyQt5 to easily get color input from the user.

![colorpicker](https://user-images.githubusercontent.com/71983360/95017068-408f8100-0657-11eb-8001-a6788e94abba.png)


## Usage

1. To use the Color Picker Widget in a python project make sure you have the `PyQt5` library:

   ```
   pip install PyQt5
   ```

   then add the `colorpicker` folder into your project folder and import `ColorPicker`

   ```python
   from colorpicker import ColorPicker
   ```

2. To ask for a color first create an `QApplication`:

   ```python
   app = QApplication([])
   ```

   then simply create an instance of the class:

   ```python
   my_color_picker = ColorPicker()
   ```

   and then run the `getColor` method:

   ```python
   picked_color = my_color_picker.getColor()
   ```


* `getColor` returns a tuple of RGB values ranging from 0 to 255, for example: `(255,0,127)`.\
  If you want the Color Picker Window to have a certain color already selected, pass an RGB tuple to it:

   ```python
   old_color = (255,255,255)
   picked_color = my_color_picker.getColor(old_color)
   ```
