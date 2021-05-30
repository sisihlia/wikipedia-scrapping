# wikipedia-scrapping


Check specs
======================
    sam init
  
Build image
======================
    sam build
    
Test image
======================
    ubuntu:~/environment/wikipedia-scrapping/wikipedia-scrap (main) $ touch payload.jso
    ubuntu:~/environment/wikipedia-scrapping/wikipedia-scrap (main) $ cat payload.json 
    {
        "entity": "twitter"
    }
    ubuntu:~/environment/wikipedia-scrapping/wikipedia-scrap (main) $ sam local invoke -e payload.json 
    Invoking Container created from helloworldfunction:python3.8-v1
    Building image.................
    Skip pulling image and use local one: helloworldfunction:rapid-1.19.0.

    Loading function
    context: <__main__.LambdaContext object at 0x7fb8ce43fca0>, event: {'entity': 'twitter'}
    Response from wikipedia API: Twitter is an American microblogging and social networking service on which users post and interact with messages known as "tweets".
    END RequestId: 2c3e1021-4c98-466d-bb0d-cef4ce0e25e4
    REPORT RequestId: 2c3e1021-4c98-466d-bb0d-cef4ce0e25e4  Init Duration: 0.67 ms  Duration: 790.51 ms     Billed Duration: 800 ms Memory Size: 128 MB     Max Memory Used: 128 MB
    {"statusCode": "200", "headers": {"Content-type": "application/json"}, "body": "{\"message\": \"Twitter is an American microblogging and social networking service on which users post and interact with messages known as \\\"tweets\\\".\"}"}
    

Create and deploye lambda
======================
    ubuntu:~/environment/wikipedia-scrapping/wikipedia-scrap (main) $ sam deploy --guided
    
    
Check the lambda and the stack created    

![image](https://user-images.githubusercontent.com/8087964/120100561-ac23e280-c141-11eb-9c5d-c2c832d21231.png)

![image](https://user-images.githubusercontent.com/8087964/120100603-dd041780-c141-11eb-91c9-81bc8b99912b.png)

The created lambda can be tested both from aws console and aws cloud9
![image](https://user-images.githubusercontent.com/8087964/120100667-2eaca200-c142-11eb-8c7a-9b8188861c0d.png)

![image](https://user-images.githubusercontent.com/8087964/120100700-53087e80-c142-11eb-84b3-4afc5026f6a1.png)


