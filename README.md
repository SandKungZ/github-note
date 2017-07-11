# github-note
Description command to use often. <br />
## Local Git
git config --global user.name "YOURNAME" <br/>
git config --global user.email "your@email.com" <br/>
git config --list <br/>

echo "# test" >> README.md		//สร้างไฟล์ readme.md

git init		//create git repository <br/>
git status		//check status git

git add index.html	//add เฉพาะเจาะจงไฟล์ <br/>
git add .		//add ไฟล์ทั้งหมด <br/>
git add '*.txt'	//*.txt ไฟล์ทั้งหมด<br/>
เราสามารถ ignore ได้ว่าจะให้ git ไม่ต้องเก็บไฟล์ไหน โดยสร้างไฟล์ชื่อ .gitignore ไว้ที่ root folder ภายในก็กำหนดค่าเช่น *.log ไม่ต้องเก็บไฟล์ .log ทั้งหมดไว้บน git เป็นต้น

git commit -m "your message"<br/>

git branch create_new_page	//สร้างสาขา<br/>
git branch		//ดูสาขาทั้งหมด<br/>
git branch -d branch_name	//ลบสาขา<br/>

git checkout branch_name	//เลือกสาขา<br/>
git checkout -b create_new_page		//สร้างแล้วเลือก<br/>

git merge create_new_page	// รวมไฟล์ ก่อนใช้ต้องเลือก สาขาหลักก่อน git checkout master<br/>

## Server Git
git remote -v	//เช็ค git host location
git remote add origin https://github.com/poonsak58/git101.git	//เพิ่ม git host location
git push -u origin master	//อัพโหลดขึ้นโฮส	-u : เอาไว้จำ parameter origin master ต่อไปก็แค่พิมพ์ git push	origin : คือชื่อ alias ของ remote (github)	master : คือชื่อ branch ที่เราต้องการ push ขึ้นไป

git fetch	//เช็คโค้ด local กับ host ตรงกันหรือไม่
git status
git merge origin/master	//ดาวโหลดไฟล์อัพเดท จาก origin สาขา master

git pull	//ดาวโหลดไฟล์อัพเดท

git clone https://github.com/poonsak58/git101.git	//ก๊อปปี้โปรเจคจากโฮส
## First Time and have project on local
git init
git add .
git commit -m "your message"
git remote add origin https://github.com/poonsak58/git101.git
git remote -v
git push -u origin master

## When server have update. Then check update local match server?
git fetch
git status			// แสดงรายละเอียดของ git local ว่าเก่าหรือใหม่กว่า origin (host)
git merge origin/master	// หรือจำใช้ git pull ก็ได้ มันคือการใช้คำสั่ง git fetch ต่อด้วย git merge origin/master
## When local have update. Then upload to server.
git add .
git commit -m "your message"
git push
git status			// แสดงรายละเอียดของ git local ว่าเก่าหรือใหม่กว่า origin (host)
