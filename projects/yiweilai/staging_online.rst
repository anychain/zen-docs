
root@staging-webservice:/var/www/html# mkdir media
root@staging-webservice:/var/www/html# cd media/
root@staging-webservice:/var/www/html/media# ls
root@staging-webservice:/var/www/html/media# mkdir images
root@staging-webservice:/var/www/html/media# mkdir pages
root@staging-webservice:/var/www/html/media# mkdir posters
root@staging-webservice:/var/www/html/media# cd pages/
root@staging-webservice:/var/www/html/media/pages# ls
root@staging-webservice:/var/www/html/media/pages# mkdir news
root@staging-webservice:/var/www/html/media/pages# mkdir activity
root@staging-webservice:/var/www/html/media/pages# 
root@staging-webservice:/var/www/html/media/pages# 
root@staging-webservice:/var/www/html/media/pages# cd


for zen-web and zen-web-admin:
zensite/libs/context.py
def get_zen_api():
    '''
        get the zen api host, port, protocol
    '''
    # todo: get api host from register server or configuration file
    return {'host': '127.0.0.1', 'port': 9081, 'protocol': 'http'}


zen-common:
/opt/zen/zen-common/zencomm/db/api.py
db_regexp_op = _get_regexp_op_for_connection('postgresql')


zen-api:
/ws/db/migration/alembic.ini
sqlalchemy.url =postgresql://yiweilai:zhu88jie@172.16.110.3:5432/yiweilai

/opt/zen/zen-api/ws/db/api.py:

return db_session.EngineFacade(
        sql_connection='postgresql://yiweilai:zhu88jie@172.16.110.3:5432/yiweilai',


connect to yiweilai database and drop table alembic_version;


change MEDIA_URL, else we can not access images and htmls
