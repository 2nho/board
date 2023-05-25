java, spring ,jQuery ,datatable, bootstrap , mybatis , mysql   


2글자의 단어도 검색을 위한 my.ini 설정 

ft_min_word_len = 2  
innodb_ft_min_token_size = 2  

# db설정
src/main/webapp/WEB-INF/properties/db.properties 
에서 설정을 맞게 변경


# board  
 * 게시판은 게시글의 ID, 제목, 본문, 생성날짜로 구성되며 제목과 본문은 각각 텍스트 입니다.
 * 게시글은 연관 게시글이라는 항목을 가지고 있으며, 연관게시글은 게시글과 내용이 유사한 게시글 입니다.
 * 하나의 게시글은 여러개의 연관게시글을 가질 수 있으며, 하나도 없을 수 있습니다.
 * 게시글목록은 게시글 제목과 날짜정보를 가져옵니다.
 * 게시글이 생성되면 연관게시글을 찾아서 연결합니다.
 * 연관게시글은 게시글의 내용을 단어별로 나눠서 각 단어가 다른 게시글에서 얼마나 많이 나타나는지를 기준으로 합니다.
 * 단, 문장에 자주쓰이는 단어를 배제하기 위해서 전체게시글 중에 60%이상에서 발견되는 단어는 연관게시글을 파악할때 사용하지 않습니다.
 * 연관게시글이 되는 기준은 40% 이하 빈도 단어가 두개이상 동시에 나타나는 것입니다.
 * 그리고, 게시글에 40% 이하 빈도로 나타나는 단어는 자주 나타날수록 더 연관이 있는 것으로 계산합니다.
 * 마지막으로 연관게시글에서 40% 이하 빈도로 나타나는 단어중 연관단어가 그렇지 않은 단어보다 더 빈번하게 나타날수록 연관이 더 있는것으로 파악합니다.
 * 게시글을 작성하고, 목록을 보여주고, 내용을 보여주는 프로그램을 만들어주시고, 게시글내용과 연관 게시글을 같이 표시해주세요.
 * 연관게시글이 보여지는 순서는 연관도가 높은것을 우선적으로 보여주도록 만들어주시면 더 좋습니다

 

