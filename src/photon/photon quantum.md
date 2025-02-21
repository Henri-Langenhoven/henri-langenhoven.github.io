# Photon Quantum

## Assigning an EntityPrototype to an AssetRef<EntityPrototype> in the Inspector

In Quantum 3.0.1 (haven't tested in later versions), I kept getting a "missing asset" error when I tried dragging a generated EntityPrototype onto a AssetRef<EntityPrototype> property in the Inspector.
I finally figured out that to be able to reference an EntityPrototype (generated when you drag e.g. a GameObject named `YourGameObject` from the Hierarchy into the Project, i.e. creating a Prefab), you have to select the generated `YourGameObjectEntityPrototype` and set the `QuantumAsset` label on it manually. This is not mentioned in the documentation at all (since maybe it's fixed in the latest versions of Quantum 3).