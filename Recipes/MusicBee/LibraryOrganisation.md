# Library Organisation

## Configure the `disc-track#` format
1. Go to `Edit` > `Edit Preferences`;
2. Go to `Tags (2)` section;
3. Go to `tag handling` subsection;
4. Go to `Configure Fields`;
5. Go to `formatting` subsection;
6. Set `disc-track# format` to `0` - `00`.

## Configure the file naming char mapping
1. Go to `Edit` > `Edit Preferences`;
2. Go to `Library` section;
3. Go to `music library` subsection;
4. Enable `auto-organise media files`;
5. Go to `Organization`;
6. Got to `Filename Char Mapping`;
7. Set `"` to no character;
8. Set `:` to no character.

## Configure the file naming
1. Go to `Edit` > `Edit Preferences`;
2. Go to `Library` section;
3. Go to `music library` subsection;
4. Enable `auto-organise media files`;
5. Go to `Organization`;
6. Set `move` to `music`, `on drive` `C:\`, `to folder` `D:\Users\Matthias\Music\Media\`;
7. Set `move` to `music`, `on drive` `D:\`, `to folder` `D:\Users\Matthias\Music\Media\`;
8. Set both `naming template`s to

```$Group($Sort(<Album Artist>),1)\<Album Artist>\<Album>\$IsNull(<Disc-Track#>,,<Disc-Track#>" ")$If($Contains(<Title>,/),$Split(<Title>,:,1),<Title>)```

`A: B` titles will be mapped to `A: B`, whereas `A: B / C` titles will be ampped to `A` (e.g., medleys).
