# Display Title

## Create virtual tags
1. Go to `Edit` > `Edit Preferences`;
2. Go to `Tags (1)` section;
3. Go to `tag storage` subsection;
4. Go to `Define New Tags`;
5. Set `label` to `Display Title`;
6. Set `formula` to

```<Title>$IsNull(<Original Artist>,," "{color: 140,140,140}[<Original Artist>])$IsNull(<Subtitle>,," "{color: 140,140,140}[<Subtitle>])```

7. Set `label` to `Display Title (Debug)`;
8. Set `formula` to

```<Title>$IsNull(<Original Artist>,," "{color: 0,255,255}[<Original Artist>])$IsNull(<Subtitle>,," "{color: 255,0,255}[<Subtitle>])```

9. Set `label` to `Display Title (with Artist)`;
10. Set `formula` to

```<Display Title>$If(<Artist>=<Album Artist>,,"    "{color: 140,140,140}[<Artist>])```

## Configure Tracks view
1. Go to `Main Panel` > `Tracks`;
2. Go to `Set Displayed Fields...`;
3. Select `Display Title`.

## Configure Album Covers view
1. Go to `Main Panel` > `Album Covers`;
2. Go to `Configure Layout` > `Main Panel` > `Customise Panel...`;
3. Go to Show Settings

## Configure Album Panel view

1. Go to `Music Explorer`;
2. Go to `Configure Layout` > `Main Panel` > `Album Panel Settings...`;
3. Set `fields displayed` to `Display Title (with Artist)`.

## Configure TOP TRACKS view

1. Go to `Music Explorer`;
2. Go to `TOP TRACKS` > `Displayed Fields`;
3. Select `Display Title`.
