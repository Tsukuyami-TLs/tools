# Mei Asset Extraction
Last updated April 23, 2022

## Requirements
- Bluestacks (or another emulators) with Higurashi Mei installed
- Python
- Extraction and Conversion Scripts
- [AssetStudio](https://github.com/Perfare/AssetStudio/releases)

## Getting the Assets from the Game
1. Update Higurashi Mei to the newest version
2. Open ”Media Manager” and click on ”Explore”
3. Navigate to ”Android/Data/com.dtechno.higurashi.mei/files/data”
4. Select all files and extract

## Extracting The Assets from the .bin files
1. Move .bin files into the ”HigurashiMeiAssetExtraction” Folder
2. Run ”execute.bat”. Assets will be extracted into the ”out” folder
3. (Optionally make a copy of the assets in the ”out-old” folder so you can
later use something like ”WinMerge” to find out what’s been added in
releases.)

## Extracting ”.unity3d” files
1. Start AssetStudio
2. Drag the ”out” folder into AssetStudio. Wait for import to finish (may take a while)
3. Click on ”Export/All Assets”
4. Select the ”extract” folder to export to
Now all scripts, sounds and some images are extracted. To assemble ADV
sprites do the following.

## Assembling ADV Sprites
1. Move ”x.atlas.prefab” and ”x.prefab” files into the
”1HigurashiMeiScriptExtractor/sprites/atlases” folder
2. Move ”x.png” file into the
”1HigurashiMeiScriptExtractor/sprites/images” folder
3. Run ”execute.bat”. Sprites will be extracted to ”characters/sprites”,
Riggings to ”characters/riggings”
4. (Copy those files into the ”game” folder)

# Mei Google Sheet Creation
Last updated April 23, 2022.
## Requirements
- Python
- Extraction and Conversion Scripts

## Converting .bytes script files to .csv files
1. Find the .bytes files. If you used our extractor they are in the
”extract/assets/assetbundle/bytes” folder.
2. Copy the scripts you want to the ”HigurashiMeiScriptExtraction” folder
3. (optional - add translation for character names to the dictionary
in ”extract-lines.py”)
4. Run ”execute.bat”. The .csv files will be created in the ”out” folder

## Uploading .csv Files to the Sheet
1. Click on ”Data” (top left), then select ”Import” and click on ”Upload”.
2. Drag first .csv file onto the window
3. Change ”Create new table” to ”Create new sheet(?)” and import
4. Repeat for all .csv files
