# Snippets

[[debugging]] 

## Create debug lines for the grid

```typescript
const createDebugTile = (
 x: number,
 y: number,
 width: number,
 height: number,
 ) => {
	 const debugTile = new Graphics()
	 debugTile.beginFill(0x000000, 0)
	 debugTile.lineStyle(2, 0x0)
	 debugTile.drawRect(x, y, width, height)
	 debugTile.endFill()
	 debugTile.alpha = 1

	 const debugTileEntity = new Entity(debugTile)
	 LayerManager.addToLayer(LayerType.Debug, debugTileEntity)
	 this._entites.push(debugTileEntity)
 }