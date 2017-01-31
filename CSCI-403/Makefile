# Change this to the correct project number
PROJECT_NUM=2
USERNAME=jonathanevans
SQLFILE=project$(PROJECT_NUM).sql
ZIPFILE=project$(PROJECT_NUM).zip

all: $(SQLFILE)

run: $(SQLFILE)
	psql postgresql://$(USERNAME)@flowers.mines.edu/csci403 -f $(SQLFILE)

zip:
	zip $(ZIPFILE) $(SQLFILE) README
