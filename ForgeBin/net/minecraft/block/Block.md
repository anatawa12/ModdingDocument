# public class Block
ブロックの種類をインスタンスで示し、動きを定義するクラス
独自の情報を持ちたい場合はTileEntityを使う必要がある

## フィールド
### public static final RegistryNamespaced blockRegistry
Minecraft本体のアイテムレジストリ。  
基本的にForgeのGameRegistryを利用するため使用しない。

### protected String textureName
Block setBlockTextureName(String textureName)やString getTextureName()をアクセサとするフィールド

### public static final Block.SoundType soundTypeStone
石のSoundType
標準のSoundTypeになる

### public static final Block.SoundType soundTypeWood
木製のもので使われているSoundType

### public static final Block.SoundType soundTypeGravel
土, 砂利, 粘土で使われているSoundType

### public static final Block.SoundType soundTypeGrass
草, 苗木, スポンジ, 枯れ木, 花, きのこ, TNT, サトウキビ, 蔦, 菌糸, スイレンの葉, 干し草の俵で使われているSoundType

### public static final Block.SoundType soundTypePiston
石のハーフブロック, 苔石, 黒曜石, (ダイヤモンド,赤石,エメラルド,ネザー水晶)鉱石, かまど, 感圧板, 石のボタン, ジュークボックス, ネザーラック系, エンドストーン, ドラゴンエッグ, エンダーチェスト, スケルトンの頭蓋骨, ドロッパー, 色付き粘土, 堅焼き粘土, 石炭ブロックで使われているSoundType

### public static final Block.SoundType soundTypeMetal
各レール, (金,鉄,ダイヤ,エメラルド,赤石)ブロック, モンスタースポナー, 鉄ドア, 鉄格子で使われているSoundType

### public static final Block.SoundType soundTypeGlass
各ガラス, 各氷, グローストーン, ネザーポータル本体, エンドポータル(枠), RSランプで使われているSoundType

### public static final Block.SoundType soundTypeCloth
各羊毛, サボテン, ケーキ, カーペットで使われているSoundType

### public static final Block.SoundType soundTypeSand
砂, ソウルサンドで使われているSoundType

### public static final Block.SoundType soundTypeSnow
各雪で使われているSoundType

### public static final Block.SoundType soundTypeLadder
はしごで使われているSoundType

### public static final Block.SoundType soundTypeAnvil
金床で使われているSoundType

### protected boolean opaque
boolean isOpaqueCube()と同義
デフォルト値: コンストラクタが呼ばれた時点でのisOpaqueCubeの戻り値

### protected int lightOpacity
このブロックで減衰する光の大きさ
デフォルト値: opaqueなら255, 違うなら0

### protected boolean canBlockGrass
デフォルト値: materialのboolean getCanBlockGrass()の否定

### protected int lightValue
このブロックの明るさ
基本的にpublic int getLightValue(IBlockAccess world, int x, int y, int z)を介してアクセスされるのでそちらをoverrideでも問題ない

### protected boolean useNeighborBrightness
不明
Flag if block should use the brightest neighbor light value as its own

### protected float blockHardness
ブロックの硬さ
public float getBlockHardness(World, int, int, int)で取得されるのこちらのoverrideで問題なし
要検証: コメントには「ブロックを壊すのに必要なヒット数を示します。」とあるので素手での回数を示すものかもしれない

### protected float blockResistance
爆発耐性
setResistanceで指定した値の3倍の値

### protected boolean blockConstructorCalled
Unsafe系のクラスからnewされたかどうかを判別する

### protected boolean enableStats

Return the state of blocks statistics flags - if the block is counted for mined and placed.
(public boolean getEnableStats()のjavadoc)の値

### protected boolean needsRandomTick
植物の成長などで使用されるRandomTickをこのブロックに対して実行するか

### protected boolean isBlockContainer;
TileEntityを持つかどうか。多くの場合BlockContainerが勝手にtrueにしている

### protected double minX;
### protected double minY;
### protected double minZ;
### protected double maxX;
### protected double maxY;
### protected double maxZ;

setBlockBoundsで指定するBlockBound

### public Block.SoundType stepSound;
上を歩くときの音
### public float blockParticleGravity;
### protected final Material blockMaterial;
ブロックのマテリアル
地図上の扱いなどを定義する

### public float slipperiness;
上を歩くときの速度(?)
デフォルト値: 0.6

### private String unlocalizedName;
setBlockNameで指定した名前

### @SideOnly(Side.CLIENT) protected IIcon blockIcon;
ブロックのテクスチャのIIcon

### private static final String \_\_OBFID = "CL_00000199";
難読化のID

### public final cpw.mods.fml.common.registry.RegistryDelegate\<Block\> delegate
?
