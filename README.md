# FRC Circuit Diagram Library

This repository contains custom component definitions for FRC (FIRST Robotics Competition) parts, designed for use with the [Circuit Diagram](https://www.circuit-diagram.org/) application.

## Structure

- **ControlSystem/**: Components like RoboRIO, Radio, RSL.
- **Power/**: Components like PDP, VRM, Battery, Breakers.
- **Motors/**: Motor controllers like Spark MAX, Talon FX, Victor SPX.
- **Sensors/**: Encoders, Gyros, Limit Switches.

## How to Use

1. Download the XML files for the components you need.
2. Place them in your Circuit Diagram "Custom Components" folder (usually `Documents/Circuit Diagram/Components`).
3. Restart Circuit Diagram.
4. The components will appear in the toolbox under their respective categories (e.g., "FRC Control System").

## Development

To preview components without installing them, use the Circuit Diagram CLI tool:

```bash
dotnet run --project ../circuitdiagram/CircuitDiagram/CircuitDiagram.CLI -- component "ControlSystem/RoboRIO.xml" -o "preview.png" --autosize
```

## VS Code Extension Setup

To preview components directly in VS Code using the Circuit Diagram extension:

1.  Ensure you have the [Circuit Diagram extension](https://marketplace.visualstudio.com/items?itemName=CircuitDiagram.circuit-diagram) installed.
2.  You need a local build of the Circuit Diagram CLI (see the main [circuitdiagram](https://github.com/circuitdiagram/circuitdiagram) repo).
3.  In VS Code settings (`Cmd+,` or `Ctrl+,`), search for `circuitDiagram.executablePath`.
4.  Set the path to your local CLI executable.

    **Example (macOS/Linux):**
    ```
    /Users/yourusername/Documents/Code/PERSONAL/circuitdiagram/CircuitDiagram/CircuitDiagram.CLI/bin/Debug/net9.0/circuit-diagram-cli
    ```

    **Example (Windows):**
    ```
    C:\Users\yourusername\Documents\Code\PERSONAL\circuitdiagram\CircuitDiagram\CircuitDiagram.CLI\bin\Debug\net9.0\circuit-diagram-cli.exe
    ```
