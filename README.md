# PRODIGY_SD_01
A Temperature Conversion Program


temp = float(input("Enter the temperature value: "))
from_unit = input("Enter the current unit (Celsius, Fahrenheit, Kelvin): ").lower()
to_unit = input("Enter the unit to convert to (Celsius, Fahrenheit, Kelvin): ").lower()

# Initialize the converted temperature
converted_temp = None

# Perform the conversion based on user input
if from_unit == "celsius":
    if to_unit == "fahrenheit":
        converted_temp = (temp * 9/5) + 32
    elif to_unit == "kelvin":
        converted_temp = temp + 273.15
    elif to_unit == "celsius":
        converted_temp = temp
elif from_unit == "fahrenheit":
    if to_unit == "celsius":
        converted_temp = (temp - 32) * 5/9
    elif to_unit == "kelvin":
        converted_temp = ((temp - 32) * 5/9) + 273.15
    elif to_unit == "fahrenheit":
        converted_temp = temp
elif from_unit == "kelvin":
    if to_unit == "celsius":
        converted_temp = temp - 273.15
    elif to_unit == "fahrenheit":
        converted_temp = ((temp - 273.15) * 9/5) + 32
    elif to_unit == "kelvin":
        converted_temp = temp

# Output the result
if converted_temp is not None:
    print(f"{temp} {from_unit.capitalize()} is equal to {converted_temp} {to_unit.capitalize()}.")
else:
    print("Invalid unit entered.")
