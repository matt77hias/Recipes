# Auto-Fill Sort Tags

1. Go to `Actions` > `Actions`;
2. Click `New` to create a new action group;
3. Name the action group: `Auto-Fill Sort Tags`;
4. Add a `Format` action type;
    - Set `Field` to `ARTISTSORT`;
    - Set `Format String` to:
```
$if(%artistsort%,%artistsort%,$if($eql(%artist%,$regexp(%artist%,'^(A|An|Das|De|Der|Des|Die|Een|Ein|Eine|El|Gli|Het|Il|La|Las|Le|Les|Lo|Los|The|Un|Una|Une|Uno) (.+)','\2, \1')),%artistsort%,$regexp(%artist%,'^(A|An|Das|De|Der|Des|Die|Een|Ein|Eine|El|Gli|Het|Il|La|Las|Le|Les|Lo|Los|The|Un|Una|Une|Uno) (.+)','\2, \1')))
```
5. Add a `Format` action type;
    - Set `Field` to `ALBUMARTISTSORT`;
    - Set `Format String` to:
```
$if(%albumartistsort%,%albumartistsort%,$if($eql(%albumartist%,$regexp(%albumartist%,'^(A|An|Das|De|Der|Des|Die|Een|Ein|Eine|El|Gli|Het|Il|La|Las|Le|Les|Lo|Los|The|Un|Una|Une|Uno) (.+)','\2, \1')),%albumartistsort%,$regexp(%albumartist%,'^(A|An|Das|De|Der|Des|Die|Een|Ein|Eine|El|Gli|Het|Il|La|Las|Le|Les|Lo|Los|The|Un|Una|Une|Uno) (.+)','\2, \1')))
```
6. Add a `Format` action type;
    - Set `Field` to `COMPOSERSORT`;
    - Set `Format String` to:
```
$if(%composersort%,%composersort%,$if($eql(%composer%,$regexp(%composer%,'^(A|An|Das|De|Der|Des|Die|Een|Ein|Eine|El|Gli|Het|Il|La|Las|Le|Les|Lo|Los|The|Un|Una|Une|Uno) (.+)','\2, \1')),%composersort%,$regexp(%composer%,'^(A|An|Das|De|Der|Des|Die|Een|Ein|Eine|El|Gli|Het|Il|La|Las|Le|Les|Lo|Los|The|Un|Una|Une|Uno) (.+)','\2, \1')))
```
7. Add a `Format` action type;
    - Set `Field` to `TITLESORT`;
    - Set `Format String` to:
```
$if(%titlesort%,%titlesort%,$if($eql(%title%,$regexp(%title%,'^(A|An|Das|De|Der|Des|Die|Een|Ein|Eine|El|Gli|Het|Il|La|Las|Le|Les|Lo|Los|The|Un|Una|Une|Uno) (.+)','\2, \1')),%titlesort%,$regexp(%title%,'^(A|An|Das|De|Der|Des|Die|Een|Ein|Eine|El|Gli|Het|Il|La|Las|Le|Les|Lo|Los|The|Un|Una|Une|Uno) (.+)','\2, \1')))
```

Do not run this script if tracks could have multiple `ARTIST` and/or `COMPOSER` atoms.
