
node {       
   def workspace = pwd() 
   load "${workspace}@script/file_esb.groovy"
}



List all files from the path 

File_esb.groovy


import jenkins.*
import jenkins.model.*
import hudson.*
import hudson.model.*

def getAllFiles(rootPath) {
    def list = []
    for (subPath in rootPath.list()) {
        list << subPath.getName()
    }
    return list
}
}
}

 


Second solution

Use this in pipeline to list all files from workspace

def  FILES_LIST = sh (script: "ls   '${workers_dir}'", returnStdout: true).trim()
//DEBUG
echo "FILES_LIST : ${FILES_LIST}"
//PARSING
for(String ele : FILES_LIST.split("\\r?\\n")){ 
   println ">>>${ele}<<<"     
}


