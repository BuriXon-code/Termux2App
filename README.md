# Termux2App 📱

## About
Termux2App is a Bash script designed for **Termux**, allowing users to manage and launch Android applications via the terminal. With Termux2App, you can:
- Add applications to a custom list with package names, activities, and color tags.
- Remove applications from the list.
- Edit existing entries.
- Retrieve detailed information about saved applications.
- Launch applications directly from the terminal.
- Use an interactive menu for managing apps efficiently.

## Features
- **Interactive selection**: Navigate using arrow keys to choose applications.
- **App management**: Add, remove, edit, and view details of applications.
- **Custom color tagging**: Assign a color (0-255) to each application for better visualization.
- **Quick launching**: Open apps via Termux without manually searching for package details.
- **JSON-based storage**: Ensures lightweight and structured data handling.

![screenshot](/help.jpg)

## Installation
```sh
git clone https://github.com/BuriXon-code/Termux2App
cd Termux2App
chmod +x termux2app
mv termux2app $PREFIX/bin/termux2app
```

Now you can use the `termux2app` command anywhere in Termux.

## Usage
The script provides multiple functionalities depending on the provided parameters.

### Usage - Open an Application

![screenshot](/open1.jpg)

Running the script without parameters opens the interactive menu.
```sh
termux2app
```
Use arrow keys to navigate and **Enter** to launch an application.

To open specified app, use:
```sh
termux2app open "App Name"
```

![screenshot](/open2.jpg)

### Usage - Add an Application

![screenshot](/add1.jpg)

To add an application to the list, use:
```sh
termux2app add
```
You will be prompted to enter:
- **Application Name**
- **Package Name** ( from `pm list packages` )
- **Activity Name** ( from `dumpsys package` | if Termux has "DUMP" permission )
- **Color Code** ( 0-255 | you can preview colors using my [256colors](https://github.com/BuriXon-code/256colors) script )

### Usage - Delete an Application

![screenshot](/del1.jpg)

To remove an application:
```sh
termux2app del -name "App Name"
```
or by package name:
```sh
termux2app del -pkgname "com.example.app"
```
If no name is provided, an interactive selection menu appears.

![screenshot](/del2.jpg)

### Usage - Edit an Application
Modify an existing entry with:
```sh
termux2app edit "App Name"
```
An interactive prompt will guide you through updating details.

### Usage - Info about Applications settings

![screenshot](/info1.jpg)

View information about a specific application:
```sh
termux2app info "App Name"
```
If no name is given, an interactive menu appears for selection.

![screenshot](/info1.jpg)

## Capability
- **Tested on**: Termux running on Android 10+
- **Dependencies**:
  - `jq` (for JSON handling)
  - `termux-am`, `android-tools` and `termux-tools` (for launching applications)
  - `git` (for installation)

## Support
### Contact me:
For any issues, suggestions, or questions, reach out via:

- **Email:** support@burixon.com.pl  
- **Contact form:** [Click here](https://burixon.com.pl/kontakt.php)

### Support me:
If you find this script useful, consider supporting my work by making a donation:

[**DONATE HERE**](https://burixon.com.pl/donate/)

Your contributions help in developing new projects and improving existing tools!
