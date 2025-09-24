# XML Schema for MuJoCo MJCF files

This repository provides an XML schema for [MuJoCo's](http://www.mujoco.org/) MJCF files. It allows for validation, autocompletion, and tooltips within compatible editors.

## Usage

This schema is provided as a single file, so you can use it directly without cloning this repository.

To enable schema validation in your MJCF files, you'll need a compatible editor with an XML language server. For Visual Studio Code, it is recommended to install the [XML extension by Red Hat](https://marketplace.visualstudio.com/items?itemName=redhat.vscode-xml).

Once the extension is installed, add the `xsi:noNamespaceSchemaLocation` attribute to the `<mujoco>` element in your XML file as follows:

```xml
<mujoco xmlns:xsi="http://www.w3.org/2001/XMLSchema-instance"
        xsi:noNamespaceSchemaLocation="https://raw.githubusercontent.com/julien-blanchon/mujoco-schema/refs/heads/main/mujoco_schema.xsd">
  
  <!-- Your model definition here -->

</mujoco>
```

Your editor should now provide autocompletion and validation for your MJCF file.

## Credits

This work is based on the original schema created by [ronansgd](https://github.com/ronansgd) in the [xml-schema-mjcf](https://github.com/ronansgd/xml-schema-mjcf) repository and has been updated for the latest MuJoCo syntax. Many thanks to them for their foundational work.
