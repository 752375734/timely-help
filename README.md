
1.直接在主线程中修改UI的操作，不用headle发送信息



2.使用方法new AsyncTask<Void, Void, String>() {
            /**
             * 可以把修改主线程的UI的设置写在里边
             */
			protected void onPreExecute() {	
			};
			/**
			 * 在后台做耗时操作
			 * 
			 */
			@Override
			protected String doInBackground(Void... params) {
			}
			/**
			 * 接收来自后台的结果信息并且，回掉到主线程中
			 */
			protected void onPostExecute(String result) {
			};
		}.execute();
