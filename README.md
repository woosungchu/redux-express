#redux-express 

####Directories

	./
	├── .babelrc                # babel 설정파일
	├── build                   # 서버 빌드 디렉토리
	├── package.json 
	├── public                  # 클라이언트 디렉토리
	│    ├── bundle.js          # 컴파일된 스크립트
	│    └── index.html         # 메인 페이지
	├── server                  # 서버 디렉토리 (ES6)
	│    ├── main.js            # 서버 사이드 메인 스크립트
	│    └── routes
	│        └── posts.js       # 예제 라우터
	├── src
	│    ├── App.js             # App 컴포넌트
	│    └── index.js           # 클라이언트 사이드 메인 스크립트
	├── webpack.config.js       # webpack 설정파일
	└── webpack.dev.config.js   # webpack-dev-server 를 위한 설정파일

####References
- <https://velopert.com/1492>

####Run Scripts
	"clean": "rm -rf build public/bundle.js",
	"build": "babel server --out-dir build && ./node_modules/.bin/webpack",
	"start": "set NODE_ENV=production&&node ./build/main.js",
	"development": "set NODE_ENV=development&&node build\main.js"