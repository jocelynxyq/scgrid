# ScGrid SDK
## Usage
* load `const scgrid=require('scgrid')`;
* create mongoDB store: `await scgrid.createStore('mongodb://localhost:27017/db')`;
* create instance `const instance = new scgrid.ScGrid(username);`
* method available on instance, e.g. `await instance.login(password)`
* all methods except `download` return a Promise

**please create mongoDB store at entry file and there is no need to create again in other files**

**If not store with mongoDB, data will be stored in memory and will lost after program restart**

## API List
* login(password, remember = true, validtime = 10)
* loginOAuth(openid, token)
* logout()
* refresh()
* calcList(appname)
* jobList()
* changeJobStatue (gid, statue)
* jobStatue (gid, callback)
* deleteJob(gid)
* jobInfo(gid)
* submitTask(dataOption)
* fileList(gid)
* upload(gid,file)
* **download(gid, file) -> return file stream**
