# CBM database

compilation of all the older databases that use `microsoft access` store types.

Here are the dropbox files provided by bert, first the access databases

```
# 2019
- https://www.dropbox.com/scl/fi/qe0g2aprk1qvuroa1lwa0/camp-2019-for-tim.accdb?rlkey=un4mel54l8f5eudzxh51cmeak&st=gf08c124&dl=0

# 2018
- https://www.dropbox.com/scl/fi/bnyc10i3rbxywp7yap9vr/camp-2018-for-tim.accdb?rlkey=6cg8zuhmafdvxyq1tiichyta2&st=u1kme05g&dl=0

# 2017
- https://www.dropbox.com/scl/fi/9ntpp67xd61ww0b6djk7n/camp-2017-for-tim.accdb?rlkey=h7tx1ttky5jrtio52fue4ici4&st=66oswphx&dl=0
```

Second the excel sheets for assignments

```
# 2019
- https://www.dropbox.com/scl/fi/kxqr4jxed13g4nnnswp8w/Cabin-Assignments-2019.xlsx?rlkey=3eow5d7e7y11jm73wzc67vi99&st=6w1rgc2x&dl=0

# 2018
- https://www.dropbox.com/scl/fi/kxqr4jxed13g4nnnswp8w/Cabin-Assignments-2019.xlsx?rlkey=3eow5d7e7y11jm73wzc67vi99&st=6w1rgc2x&dl=0


# 2017
- https://www.dropbox.com/scl/fi/jdgnix1i6btdbjwvr99vv/Cabin-Assignments-2017-073017.xlsx?rlkey=64csa7gcwx5ch75dxgebia3q9&st=kbt6werh&dl=0
```

## How to Export (requires a Windows Machine + MS Office)

Open the database with `MS Access` an offline database tool made by `microsoft`

1. Export the `General Information` data sheet with the most rows as `xslx` which can be read by python
2. Export the the `HS` for high school, and `JH` for middle school, as `xslx` which can be read by python

## Ask (in 2019):

```
this year, instead of google forms, we're using an actual online registration provider, http://regfox.com. they allow exporting of the reg data to csv. i need a way to import it into the db. i don't have a sample csv yet. i'm still learning how to use regfox and am in the process of building the reg page.

automate updating the db with the cabin and counselor assignments. during cabin assignment night aka draft night, we display the cabin assignments spreadsheet on a large screen for everyone to see and we move names around. when the spreadsheet is done, i manually update each camper with their cabin and counselor assignment info.

automate rec team assignments. i do some special sorting but then i manually go through the form and assign everyone a team.
```


## Short Term Goals

```
eval the db structure to see if anything can be improved. split up the table? add relationships? before i sent you the db, i deleted the values in the Provider and PolicyNumber fields. those contained health insurance information that i probably shouldn't be keeping. should that be a separate table? that's why the filename has "for tim" in it.

find a better way to record a camper's counselor. right now, i use a query to build a list of the counselors' names, but that field doesn't actually point to a counselor's record.
```

## Long Term Goals
```
instead of a db per camp year, create one unified database with a year field.

long term goal #1 will allow checks like seeing if a camper is getting a counselor for a 2nd time.

long term goal #1 allows us to do analytics like seeing a camper's counselor history, or seeing a counselor's camper history.
automate cabin assignments. allow the directors to manually assign certain campers to a cabin and counselor. then use code to place the remaining campers.

make the db easy to use so that someone without access experience can use it.
```


# Setting up `python` with `pyenv`

```sh
pyenv install 3.11.8
pyenv virtualenv 3.11.8 cbm-db-3.11.8
echo cbm-db-3.11.8 > .python-version
pip install -r requirements.txt
```