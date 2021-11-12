# REST_API_TEST_ctrlX_PLC
##Python example code to ctrlX PLC Engineering API
### start the code:
import requests# import requests after we have installed it
import json #to transfer the response into json format
ProjectClose={
  "jobType": "ProjectJob",
  "jobParameters": {
    "action": "Close"
  }
}
url='http://localhost:9002/plc/engineering/api/v2/jobs'
response = requests.post(url,json=ProjectClose)#sent the requests to REST API 
print(response.json())

















#define the command as json format
# ImportPlcOpenXml={
#   "jobType": "ImportPlcOpenXmlJob",
#   "jobParameters": {
#     "nodeUrl": "/devices/device/PLC Logic/Application",
#     "filePath": "D:\\mine\\Api\\XML_Files",# This is the Path of the projekt 
#     "fileName": "Test.xml"# the projekt name 
#   }
# }
# url='http://localhost:9002/plc/engineering/api/v2/jobs'# url for Jobs 
# response = requests.post(url,json=ImportPlcOpenXml)#sent the requests to REST API 
# print(response.json())









































# # delete the GVL from the Application root
# url='http://localhost:9002/plc/engineering/api/v2/devices/Device/PLC%20Logic/Application/GVL'# the URL of GVL
# response = requests.delete(url)# sent the delete requests to the REST API 






































#gvl is defined as dictionaries this corresponds to the JSON format with the corresponding changes
# gvl={
#   "name": "GVL",
#   "elementType": "GVL",
#   "elementProperties": {
#     "build": {
#       "excludeFromBuild": False,
#       "external": False,
#       "enableSystemCall": False,
#       "linkAlways": False,
#       "compilerDefines": ""
#     }
#   },
#   "declaration": "{attribute 'qualified_only'}\nVAR_GLOBAL\n AM_FROM_Python: BOOL := FALSE ; \n END_VAR"# Modify data
# }
# url='http://localhost:9002/plc/engineering/api/v2/devices/Device/PLC%20Logic/Application/GVL'# the URL of the GVL 
# response = requests.put(f'{url}',json=gvl)# sent a PUT requests to the REST API 
# print(response.json())#  to see the REST API response 




























# url='http://localhost:9002/plc/engineering/api/v2/devices/Device/PLC%20Logic/Application/PLC_PRG'# the URL of the PLC_PRG 
# response=requests.get(f'{url}')# sent the git requests to the REST API
# print(f"The REST API rsepone is \n {response.json()}")# print the response in the Console in json format 
