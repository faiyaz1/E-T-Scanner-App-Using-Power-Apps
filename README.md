# E&T-Scanner-App-Using-Power-Apps
![Screenshot 2021-06-19 at 9 01 27 PM](https://user-images.githubusercontent.com/26791884/122647386-a8ccb700-d141-11eb-941c-4a7a90afb73c.png)

Scans barcodes, QR codes, and data-matrix codes on an Android or iOS device.

**Description**
The control opens a native scanner on an Android or iOS device. The scanner automatically detects a barcode, a QR code, or a data-matrix code when in view. The control doesn't support scanning in a web browser.

**Key properties**
**Value** – Output property that contains the text value of the code that was scanned most recently.

**Type** – Output property that contains the type of the code that was scanned most recently.

**OnScan** – How an app responds when a barcode is successfully scanned.

**BarcodeType** - The barcode type to scan. You can target multiple barcode types by concatenating them. Ex. BarcodeType.Code128 & BarcodeType.Code39 Default: Auto

**FlashlightEnabled** - Whether the flashlight is enabled automatically when the scanner is opened.

**Function**

**Set ** - Simplest to use.Holds a number, text string,Boolean,record,table,etc. that can be refrences from anywhere in the app.
      Scope -- App level
      Variable type -- Golbal Variable
      ![Screenshot 2021-06-16 at 9 07 21 PM](https://user-images.githubusercontent.com/26791884/122647755-5e4c3a00-d143-11eb-92bc-5b0f868aa376.png)
**Launc** -- Webpages are launched via a URL address. For example:
             Launch( "https://bing.com" )
             ![Screenshot 2021-06-16 at 9 07 29 PM](https://user-images.githubusercontent.com/26791884/122647858-eb8f8e80-d143-11eb-8f20-e252aebd1213.png)
Collect

The Collect function adds records to a data source. The items to be added can be:
A single value: The value is placed in the Value field of a new record. All other properties are left blank.
A record: Each named property is placed in the corresponding property of a new record. All other properties are left blank.
A table: Each record of the table is added as a separate record of the data source as described above. The table isn't added as a nested table to a record. To do this, wrap the table in a record first.
When used with a collection, additional columns will be created as needed. The columns for other data sources are fixed by the data source and new columns can't be added.
If the data source doesn't already exist, a collection is created.
![Screenshot 2021-06-16 at 9 07 51 PM](https://user-images.githubusercontent.com/26791884/122647905-37dace80-d144-11eb-82bd-ab030a372c18.png)

**Patch**  Modifies or creates one or more records in a data source, or merges records outside of a data source.
Use Patch with the Defaults function to create records.
Patch( Customers, Defaults( Customers ), { Name: "Contoso" } )
To use this function with a data source, specify the data source, and then specify a base record.

To modify a record, the base record needs to have come from a data source. The base record may have come through a gallery's Items property, been placed in a context variable, or come through some other path. But, you can trace the base record back to the data source. This is important as the record will include additional information to help find the record again for modification.

To create a record, use the Defaults function to create a base record with default values.
![Screenshot 2021-06-16 at 9 07 59 PM](https://user-images.githubusercontent.com/26791884/122648030-d23b1200-d144-11eb-8993-b5bc84536877.png)
