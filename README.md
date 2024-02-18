
# python mongoDB ATLAS basic connection


<p align="center">
    <img src="./ss_atlas1.png" alt="atlas1" style="display: block; margin: 0 auto;">
</p>

<p align="center">
    <img src="./ss_atlas2.png" alt="atlas2" style="display: block; margin: 0 auto;">
</p>

<p align="center">
    <img src="./ss_atlas3.png" alt="atlas3" style="display: block; margin: 0 auto;">
</p>


## Begin Project:

    ❯ python -m venv venv

    ❯ source ./venv/bin/activate

    ❯ python -m pip install pymongo




[do project]

    ❯ vim pymongo_testconn.py

    from pymongo.mongo_client import MongoClient
    from pymongo.server_api import ServerApi

    uri = "mongodb+srv://ammongodb:**********@cluster0.******.mongodb.net/"

    # Set the Stable API version when creating a new client
    client = MongoClient(uri, server_api=ServerApi('1'))

    try:
        client.admin.command('ping')
        print("Pinged your deployment. You successfully connected to MongoDB!")
    except Exception as e:
        print(e)



## Run

    ❯ python3 pymongo_testconn.py


<p align="center">
    <img src="./ss_pymongo_testconn.png" alt="result" style="display: block; margin: 0 auto;">
</p>