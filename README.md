# Flutter Country Calling Code Picker

Searchable country picker widget ready to use in a dialog, bottom sheet and even in full screen!

1. Import the plugin using

   ```
   import 'package:country_calling_code_picker/picker.dart';
   ```
   
2. Initialize your UI using default country.

   ```
   void initCountry() async {
    final country = await getDefaultCountry(context);
    setState(() {
      _selectedCountry = country;
    });
   }
   ```
   
3. Use utility function showCountryPickerSheet to show a bottom sheet picker.

   ```
   void _showCountryPicker() async{
    final country = await showCountryPickerSheet(context,);
    if (country != null) {
      setState(() {
        _selectedCountry = country;
      });
    }
   }
   ```
   
4. Use utility function showCountryPickerDialog to show a dialog.

   ```
   void _showCountryPicker() async{
    final country = await showCountryPickerDialog(context,);
    if (country != null) {
      setState(() {
        _selectedCountry = country;
      });
    }
   }
   ```
   
5. CountryPickerWidget can be used for showing in a full screen.

   ```
   class PickerPage extends StatelessWidget {
   @override 
   Widget build(BuildContext context) {
   return Scaffold(
   appBar: AppBar(
   title: Text('Select Country'),
   ),
   body: Container(
   child: CountryPickerWidget(
   onSelected: (country) => Navigator.pop(context, country),
   ),
   ),
   );
   }
   }
   ```
