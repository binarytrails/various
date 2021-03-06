#! @file
#! @author Vsevolod Ivanov

CXX=g++
CXXFLAGS=-Wall -Wextra -Wfatal-errors -pedantic -g \
		-lasan -lopendht -lgnutls -pthread -ljsoncpp -I/usr/include/opendht \
		-DOPENDHT_JSONCPP -DASIO_STANDALONE

putget:
	${CXX} ${CXXFLAGS} -std=c++11 putget.cpp -o putget.out

proxy_pistache:
	${CXX} ${CXXFLAGS} -std=c++11 \
		dhtproxyserver/proxy_pistache.cpp -I./dhtproxyserver \
		-lpistache -I/usr/include/pistache \
		-o proxy_pistache.out

proxy_cpr:
	${CXX} ${CXXFLAGS} -std=c++11 \
		dhtproxyserver/proxy_cpr.cpp -I./dhtproxyserver \
		-lcpr -I/usr/include/cpr -lmongoose -I/usr/include \
		-o proxy_cpr.out

proxy_restinio:
	${CXX} ${CXXFLAGS} -std=c++14 \
		dhtproxyserver/proxy_restinio.cpp -I./dhtproxyserver \
		-I/usr/local/include/restinio -lfmt -lhttp_parser \
		-o proxy_restinio.out

crypto:
	${CXX} ${CXXFLAGS} -std=c++14 crypto.cpp -o crypto.out

dhtclient:
	${CXX} ${CXXFLAGS} -std=c++14 dhtclient.cpp -o dhtclient.out

dhtclient_async:
	${CXX} ${CXXFLAGS} -std=c++14 dhtclient_async.cpp -o dhtclient_async.out

proxy_runner:
	${CXX} ${CXXFLAGS} -std=c++14 proxy_runner.cpp -o proxy_runner.out

future_get:
	${CXX} ${CXXFLAGS} -std=c++14 future-get.cpp -o future-get.out

http:
	${CXX} ${CXXFLAGS} -lhttp_parser -std=c++14 -lcrypto http.cpp -o http.out

http_errors:
	${CXX} ${CXXFLAGS} -lhttp_parser -std=c++14 -lcrypto http_errors.cpp -o http_errors.out

https:
	${CXX} ${CXXFLAGS} -lhttp_parser -std=c++14 -lssl -lcrypto http.cpp -o https.out

https_2waystls:
	${CXX} ${CXXFLAGS} -lhttp_parser -std=c++14 -lssl -lcrypto https_2waystls.cpp -o https_2waystls.out

clean:
	rm -f *.out
