# Changelog
All notable changes to this project will be documented in this file.

## Release 2.1.1

### Bugfix
- Legacy bindings of ValueDisplay elements within UI did not work if deployed with VS Code AppSpace SDK
- UI differs if deployed via Appstudio or VS Code AppSpace SDK
- Fullscreen icon of iFrame was visible

## Release 2.1.0

### Improvements
- Custom functions (like stringPack, stringUnpack, searchAndCut) can be used in combination with other functions (e.g. tonumber(stringUnpack('I2', stringPack('I2', param1)))
- Removed temp data from persistent parameters

### Bugfix
- Expression function "tonumber" was not able to handle float values
- Merge data mode still active after switching mode within FlowConfig block

## Release 2.0.0

### New features
- Supports FlowConfig feature to receive data / forward results
- Added new syntaxes: 'stringPack', 'stringUnpack', 'searchAndCut', 'dateTime', 'timestamp'
- New feature to merge multiple parameters of different events and to provide them within a single event with multiple parameters (see 'setMergeData' and 'OnNewData_EXPRESSION')
- New feature to provide the result of the expression criteria ('OnNewCriteriaResult_EXPRESSION')
- New feature to only forward result if criteria is valid ('setCheckCriteriaToForward')
- New feature to use custom results, based on criteria ('setCustomResultMode')
- Selectable if processed data should be shown in UI ('setShowProcessData')
- Provide version of module via 'OnNewStatusModuleVersion'
- Function 'getParameters' to provide PersistentData parameters
- Check if features of module can be used on device and provide this via 'OnNewStatusModuleIsActive' event / 'getStatusModuleActive' function
- Function to 'resetModule' to default setup

### Improvements
- Prevent runtime error based on wrong expression definition
- extended 'addExpression' with attribute to set if it should only merge data
- proper UI table selection
- Improved behaviour for loading parameters (not needed to wait for other modules)
- New UI design available (e.g. selectable via CSK_Module_PersistentData v4.1.0 or higher), see 'OnNewStatusCSKStyle'
- 'loadParameters' returns its success
- 'sendParameters' can control if sent data should be saved directly by CSK_Module_PersistentData
- Added UI icon and browser tab information

### Bugfix
- Check if CROWN really provides XML content before trying to use it
- UI table selection runs into error for some selections
- Return value of 'OnNewResult_...' event was always 'bool' but needs to be 'auto'

## Release 1.0.0
- Initial commit