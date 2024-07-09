# Witcher 3 Settings Schema

Unofficial XML schema definition for Witcher 3's menu XMLs.


## How to use

You can use any sort of XML validation software to validate your mod menu files, but if you're a Visual Studio Code user you can install the [Red Hat's XML extension](https://marketplace.visualstudio.com/items?itemName=redhat.vscode-xml). It will give you access to autocompletion and real-time diagnostics.

Then in your XML file add the following attributes to the `UserConfig` element:
```js
xmlns:xsi="http://www.w3.org/2001/XMLSchema-instance" 
xsi:noNamespaceSchemaLocation="https://raw.githubusercontent.com/SpontanCombust/tw3-settings-schema/master/tw3-menu.xsd"
```

The document should afterwards look something like this:
```xml
<?xml version="1.0" encoding="UTF-16"?>
<UserConfig xmlns:xsi="http://www.w3.org/2001/XMLSchema-instance" xsi:noNamespaceSchemaLocation="https://raw.githubusercontent.com/SpontanCombust/tw3-settings-schema/master/tw3-menu.xsd">
	<!-- Here go Group elements -->
</UserConfig>
```

`xsi:noNamespaceSchemaLocation` can also take a file path instead of a URI if you plan to download the XSD and use it locally.
```js
xsi:noNamespaceSchemaLocation="../path/to/tw3-menu.xsd"
```


## Limitations

Complex attributes such as the `SLIDER` variant of `displayType` will not be visible in the autocompletion list in the editor when using the aformentioned VSCode extension.


## Contibutions

If you find any erros in the schema you're welcome to submit an issue and/or pull request with the fix.
