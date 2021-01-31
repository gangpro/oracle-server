# Managing Undo Data
> 언두 데이터 관리 : 11gWS1 교재 10장<br>

> 개발환경<br> 
> OS : Macbook Pro, macOS Mojave<br>
> VirtualBox : Version 6.0.4<br>
> 가상환경 : Enterprise Linux, Oracle 11g

## 
* undo advisor를 활용해서 이 서버에 필요한 undo 크기를 파악한 뒤 적절한 크기의 undo 테이블스페이스를 사용하도록 설정하는 것
###
      SQL> create undo tablespace myundo_ts
           datafile '/u01/app/oracle/oradata/orcl/undo43.dbf' size 100m;
    
      SQL> alter system set undo_tablespace = myundo_ts;
    
      SQL> show parameter undo
    
      NAME                                 TYPE        VALUE
      ------------------------------------ ----------- ------------------------------
      undo_management                      string      AUTO
      undo_retention                       integer     900
      undo_tablespace                      string      MYUNDO_TS
    
      SQL> select tablespace_name, contents
           from dba_tablespaces;
    
      TABLESPACE_NAME                CONTENTS
      ------------------------------ ---------
      SYSTEM                         PERMANENT   --> permanent : 모든 유형의 segment 보관 가능
      SYSAUX                         PERMANENT
      USERS                          PERMANENT
      EXAMPLE                        PERMANENT
      MYTS                           PERMANENT
      UNDOTBS1                       UNDO        --> undo      : 오직 undo segment만 보관 가능   
      MYUNDO_TS                      UNDO
      TEMP                           TEMPORARY   --> temporary : 오직 temporary segment만 보관 가능   
    











