# Ignore Words in Sorting

1. Go to `C:\ProgramData\Jellyfin\Server\config\system.xml`;
2. Go to the `SortRemoveCharacters` scope;
3. Add `", +`:
 ```
<SortRemoveCharacters>
    <string>"</string>
    <string>+</string>
    <string>,</string>
    <string>&amp;</string>
    <string>-</string>
    <string>{</string>
    <string>}</string>
    <string>'</string>
</SortRemoveCharacters>
```
4. Go to the `SortRemoveWords` scope;
5. Add `A, An, Das, De, Der, Des, Die, Een, Ein, Eine, El, Gli, Het, Il, La, Las, Le, Les, Lo, Los, The, Un, Una, Une, Uno`:
```
<SortRemoveWords>
    <string>a</string>
    <string>an</string>
    <string>das</string>
    <string>de</string>
    <string>der</string>
    <string>des</string>
    <string>die</string>
    <string>een</string>
    <string>ein</string>
    <string>eine</string>
    <string>el</string>
    <string>gli</string>
    <string>het</string>
    <string>il</string>
    <string>la</string>
    <string>las</string>
    <string>le</string>
    <string>les</string>
    <string>lo</string>
    <string>los</string>
    <string>the</string>
    <string>un</string>
    <string>una</string>
    <string>une</string>
    <string>uno</string>
</SortRemoveWords>
```

| Language                                                      | indefinite, singular | indefinite, plural | definite, singular | definite, plural |
|---------------------------------------------------------------|----------------------|--------------------|--------------------|------------------|
| Dutch                                                         | een                  | /                  | de, de, het        | de               |
| English                                                       | a/an                 | /                  | the                | the              |
| French                                                        | un, une              | des                | le, la             | les              |
| [German](https://en.wikipedia.org/wiki/German_articles)       | ein, eine, ein       | /                  | der, die, das      | die              |
| [Italian](https://en.wikipedia.org/wiki/Italian_grammar)      | un/uno, una/un'      | /                  | il/lo, la          | i/gli, le        |
| [Spanish](https://en.wikipedia.org/wiki/Spanish_determiners)  | un, una, uno         | unos, unas         | el, la, lo         | los, las         |
