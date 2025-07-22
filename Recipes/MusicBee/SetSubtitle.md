# Set Subtitle

## Create a virtual tag
1. Go to `Edit` > `Edit Preferences`;
2. Go to `Tags (1)` section;
3. Go to `tag storage` subsection;
4. Go to `Define New Tags`;
5. Set `label` to `Sub-Header`;
6. Set `formula` to

```$If(<Disc Count>>1,$IsNull(<Grouping>,"• Disc "<Disc#>" •","• Disc "<Disc#>" • "<Grouping>" •"),$IsNull(<Grouping>,,"• "<Grouping>" •"))```

## Use the virtual tag for the sub-grouping
1. Set `Configure Layout` > `Main Panel` > `Album Covers`;
2. Go to `Configure Layout` > `Main Panel` > `Customise Panel...`;
3. Go to `Artwork` section;
4. Go to `Show Settings`;
5. Set `sub-grouping header` to `Sub-Header`.
