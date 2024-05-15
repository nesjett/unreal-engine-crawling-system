# Setting up Player Inputs

This package is installed into existing projects and thus sometimes the control Inputs might not be set up in the Game.

While sometimes this is just fine so that you can customize them to your own game needs, it makes it difficult if you just want to use the defaults or have a fast check on the package.

Because of this. I prepared a [CrawlingSystemInputs.ini](files/CrawlingSystemInputs.ini) file that you can download and import direclty into your game configuration.

![Importing a config file](../images/import-inputs-config.jpg){ loading=lazy }

!!! note
    This Inputs file will not only add the required Inputs but also set to defaults the whole config related to Inputs.
    If you prefere not to override those configs, you can manually add the following configs:
    ```
    AxisMappings=(AxisName="Turn",Scale=1.000000,Key=MouseX)
    AxisMappings=(AxisName="LookUp",Scale=-1.000000,Key=MouseY)
    AxisMappings=(AxisName="LookUpRate",Scale=-1.000000,Key=MouseY)
    AxisMappings=(AxisName="MoveForward",Scale=1.000000,Key=W)
    AxisMappings=(AxisName="MoveRight",Scale=1.000000,Key=D)
    AxisMappings=(AxisName="TurnRate",Scale=1.000000,Key=MouseX)
    AxisMappings=(AxisName="MoveForward",Scale=-1.000000,Key=S)
    AxisMappings=(AxisName="MoveRight",Scale=-1.000000,Key=A)
    ```