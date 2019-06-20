<div id="article_content" class="article_content clearfix csdn-tracking-statistics" data-pid="blog" data-mod="popu_307" data-dsm="post">
                                    <div class="article-copyright">
                                            <svg class="icon" title="CSDN认证原创" aria-hidden="true" style="width:53px; height: 18px; vertical-align: -4px;">
                            <use xlink:href="#CSDN_Cert"></use>
                        </svg>

<p>1.</p>

<p><img alt="" class="has" height="337" src="https://img-blog.csdnimg.cn/20190502124101380.jpg?x-oss-process=image/watermark,type_ZmFuZ3poZW5naGVpdGk,shadow_10,text_aHR0cHM6Ly9ibG9nLmNzZG4ubmV0L3dlaXhpbl80MjcyMTk1Nw==,size_16,color_FFFFFF,t_70" width="820"></p>

<p><a href="https://www.zhaoj.in/wp-content/uploads/2019/05/1558435045566773b68e18d60696d1a508a503e8c3.zip" rel="nofollow" target="_blank">附件地址</a></p>

<p>下载附件显示如下：</p>

<p><img alt="" class="has" src="https://img-blog.csdnimg.cn/20190502124130808.jpg?x-oss-process=image/watermark,type_ZmFuZ3poZW5naGVpdGk,shadow_10,text_aHR0cHM6Ly9ibG9nLmNzZG4ubmV0L3dlaXhpbl80MjcyMTk1Nw==,size_16,color_FFFFFF,t_70"></p>

<p>看了半天像是ascll码，但是有的已经超出范围了。</p>

<p>然后又觉得以0开头的是八进制的数，先进制转换。发现一段字符串看着像base64加密的</p>

<p><img alt="" class="has" height="90" src="https://img-blog.csdnimg.cn/20190502125534698.jpg" width="627"></p>

<p>解密得到flag</p>

<p><img alt="" class="has" height="127" src="https://img-blog.csdnimg.cn/20190502125551824.jpg?x-oss-process=image/watermark,type_ZmFuZ3poZW5naGVpdGk,shadow_10,text_aHR0cHM6Ly9ibG9nLmNzZG4ubmV0L3dlaXhpbl80MjcyMTk1Nw==,size_16,color_FFFFFF,t_70" width="875"></p>

<p>2.Aesop's secret&nbsp;</p>

<p><img alt="" class="has" src="https://img-blog.csdnimg.cn/20190528155514390.jpg?x-oss-process=image/watermark,type_ZmFuZ3poZW5naGVpdGk,shadow_10,text_aHR0cHM6Ly9ibG9nLmNzZG4ubmV0L3dlaXhpbl80MjcyMTk1Nw==,size_16,color_FFFFFF,t_70"></p>

<p><a href="https://www.zhaoj.in/wp-content/uploads/2019/05/1558477280ec71d6dae69ff3fd67630a47b33a3615.zip" rel="nofollow" target="_blank">附件地址</a></p>

<p>下载附件打开发现是一张gif图片，查看并没有什么卵用</p>

<p><img alt="" class="has" src="https://img-blog.csdnimg.cn/2019052815560592.jpg?x-oss-process=image/watermark,type_ZmFuZ3poZW5naGVpdGk,shadow_10,text_aHR0cHM6Ly9ibG9nLmNzZG4ubmV0L3dlaXhpbl80MjcyMTk1Nw==,size_16,color_FFFFFF,t_70"></p>

<p>然后记事本打开看看，发现最后有一堆字符串，比较可疑</p>

<p><img alt="" class="has" src="https://img-blog.csdnimg.cn/20190528155640440.jpg?x-oss-process=image/watermark,type_ZmFuZ3poZW5naGVpdGk,shadow_10,text_aHR0cHM6Ly9ibG9nLmNzZG4ubmV0L3dlaXhpbl80MjcyMTk1Nw==,size_16,color_FFFFFF,t_70"></p>

<p>结合到题目的线索，猜想应该是AES加密，而且密钥应该是ISCC</p>

<p>用在线解密网站进行解密，需要经过两次才能得到flag，尝试一次就换思路的小伙伴不要太郁闷</p>

<p><img alt="" class="has" src="https://img-blog.csdnimg.cn/20190528155852588.jpg?x-oss-process=image/watermark,type_ZmFuZ3poZW5naGVpdGk,shadow_10,text_aHR0cHM6Ly9ibG9nLmNzZG4ubmV0L3dlaXhpbl80MjcyMTk1Nw==,size_16,color_FFFFFF,t_70"></p>

<p>3.最危险的地方就是最安全的地方</p>

<p><img alt="" class="has" height="340" src="https://img-blog.csdnimg.cn/20190528182643570.jpg?x-oss-process=image/watermark,type_ZmFuZ3poZW5naGVpdGk,shadow_10,text_aHR0cHM6Ly9ibG9nLmNzZG4ubmV0L3dlaXhpbl80MjcyMTk1Nw==,size_16,color_FFFFFF,t_70" width="877"></p>

<p><a href="https://www.zhaoj.in/wp-content/uploads/2019/05/15584352907afc4ab69ef3c7ca3e905903f171a46d.zip" rel="nofollow" target="_blank">附件地址</a></p>

<p>下载附件发现是一张图片，但是无法打开</p>

<p><img alt="" class="has" src="https://img-blog.csdnimg.cn/20190528182750868.jpg?x-oss-process=image/watermark,type_ZmFuZ3poZW5naGVpdGk,shadow_10,text_aHR0cHM6Ly9ibG9nLmNzZG4ubmV0L3dlaXhpbl80MjcyMTk1Nw==,size_16,color_FFFFFF,t_70"></p>

<p>用binwalk打开查看，似乎是一个压缩文件</p>

<p><img alt="" class="has" src="https://img-blog.csdnimg.cn/20190528182823904.jpg?x-oss-process=image/watermark,type_ZmFuZ3poZW5naGVpdGk,shadow_10,text_aHR0cHM6Ly9ibG9nLmNzZG4ubmV0L3dlaXhpbl80MjcyMTk1Nw==,size_16,color_FFFFFF,t_70"></p>

<p>解压缩得到50个二维码图片</p>

<p><img alt="" class="has" height="443" src="https://img-blog.csdnimg.cn/2019052818284654.jpg?x-oss-process=image/watermark,type_ZmFuZ3poZW5naGVpdGk,shadow_10,text_aHR0cHM6Ly9ibG9nLmNzZG4ubmV0L3dlaXhpbl80MjcyMTk1Nw==,size_16,color_FFFFFF,t_70" width="662"></p>

<p><img alt="" class="has" height="561" src="https://img-blog.csdnimg.cn/20190528182856660.jpg?x-oss-process=image/watermark,type_ZmFuZ3poZW5naGVpdGk,shadow_10,text_aHR0cHM6Ly9ibG9nLmNzZG4ubmV0L3dlaXhpbl80MjcyMTk1Nw==,size_16,color_FFFFFF,t_70" width="843"></p>

<p>发现别的图片都特别小，只有50格外的大，应该藏有不一样的东西，用记事本打开</p>

<p><img alt="" class="has" height="429" src="https://img-blog.csdnimg.cn/20190528182958585.jpg?x-oss-process=image/watermark,type_ZmFuZ3poZW5naGVpdGk,shadow_10,text_aHR0cHM6Ly9ibG9nLmNzZG4ubmV0L3dlaXhpbl80MjcyMTk1Nw==,size_16,color_FFFFFF,t_70" width="627"></p>

<p>看到这一段字符串，就想到了base64，解密果断得到flag</p>

<p><img alt="" class="has" src="https://img-blog.csdnimg.cn/20190528183031131.jpg?x-oss-process=image/watermark,type_ZmFuZ3poZW5naGVpdGk,shadow_10,text_aHR0cHM6Ly9ibG9nLmNzZG4ubmV0L3dlaXhpbl80MjcyMTk1Nw==,size_16,color_FFFFFF,t_70"></p>

<p>&nbsp;</p>

<p>4.倒立屋</p>

<p><img alt="" class="has" height="332" src="https://img-blog.csdnimg.cn/20190528195928549.jpg?x-oss-process=image/watermark,type_ZmFuZ3poZW5naGVpdGk,shadow_10,text_aHR0cHM6Ly9ibG9nLmNzZG4ubmV0L3dlaXhpbl80MjcyMTk1Nw==,size_16,color_FFFFFF,t_70" width="869"></p>

<p><a href="https://www.zhaoj.in/wp-content/uploads/2019/05/1558438333d13d0f8064b7d34321f7eeb53528728a.zip" rel="nofollow" target="_blank">附件地址</a></p>

<p>附件是一个倒立的屋子的图片</p>

<p><img alt="" class="has" src="https://img-blog.csdnimg.cn/20190528200145956.jpg?x-oss-process=image/watermark,type_ZmFuZ3poZW5naGVpdGk,shadow_10,text_aHR0cHM6Ly9ibG9nLmNzZG4ubmV0L3dlaXhpbl80MjcyMTk1Nw==,size_16,color_FFFFFF,t_70"></p>

<p>用记事本和hex 编辑器打开没有发现什么异常，再用&nbsp;<a href="https://github.com/zardus/ctf-tools/tree/master/stegsolve" rel="nofollow" target="_blank">StegSolve</a>&nbsp;打开看看</p>

<p><img alt="" class="has" src="https://img-blog.csdnimg.cn/20190528200122983.jpg?x-oss-process=image/watermark,type_ZmFuZ3poZW5naGVpdGk,shadow_10,text_aHR0cHM6Ly9ibG9nLmNzZG4ubmV0L3dlaXhpbl80MjcyMTk1Nw==,size_16,color_FFFFFF,t_70"></p>

<p>点 开Analyse的Data Extract，然后逐位试试，发现 RGB 都点到 0 的时候开头有一段奇怪的字符串。</p>

<p><img alt="" class="has" height="639" src="https://img-blog.csdnimg.cn/20190528200252180.jpg?x-oss-process=image/watermark,type_ZmFuZ3poZW5naGVpdGk,shadow_10,text_aHR0cHM6Ly9ibG9nLmNzZG4ubmV0L3dlaXhpbl80MjcyMTk1Nw==,size_16,color_FFFFFF,t_70" width="829"></p>

<p>直接提交当然不对，因为题目是倒立屋，所以倒过来提交就是flag。</p>

<p>5.解密成绩单</p>

<p><img alt="" class="has" height="352" src="https://img-blog.csdnimg.cn/20190528203656504.jpg?x-oss-process=image/watermark,type_ZmFuZ3poZW5naGVpdGk,shadow_10,text_aHR0cHM6Ly9ibG9nLmNzZG4ubmV0L3dlaXhpbl80MjcyMTk1Nw==,size_16,color_FFFFFF,t_70" width="850"></p>

<p><a href="https://www.zhaoj.in/wp-content/uploads/2019/05/1558446460ad65669032cbb047ef5d6aa385d20ab3.zip" rel="nofollow" target="_blank">附件地址</a></p>

<p>附件下载下来解压发现需要密码</p>

<p><img alt="" class="has" height="385" src="https://img-blog.csdnimg.cn/2019052820380869.jpg?x-oss-process=image/watermark,type_ZmFuZ3poZW5naGVpdGk,shadow_10,text_aHR0cHM6Ly9ibG9nLmNzZG4ubmV0L3dlaXhpbl80MjcyMTk1Nw==,size_16,color_FFFFFF,t_70" width="404"></p>

<p>但是题目并没有给出过多的提示，所以这里就卡住了，队友说用360压缩可以不要密码，试了一下果然可以，还没搞懂这个原理</p>

<p><img alt="" class="has" height="298" src="https://img-blog.csdnimg.cn/2019052820390433.jpg?x-oss-process=image/watermark,type_ZmFuZ3poZW5naGVpdGk,shadow_10,text_aHR0cHM6Ly9ibG9nLmNzZG4ubmV0L3dlaXhpbl80MjcyMTk1Nw==,size_16,color_FFFFFF,t_70" width="810"></p>

<p>解压出来是一个可执行文件，随便输入一个尝试了一下</p>

<p><img alt="" class="has" src="https://img-blog.csdnimg.cn/2019052820394389.jpg?x-oss-process=image/watermark,type_ZmFuZ3poZW5naGVpdGk,shadow_10,text_aHR0cHM6Ly9ibG9nLmNzZG4ubmV0L3dlaXhpbl80MjcyMTk1Nw==,size_16,color_FFFFFF,t_70"></p>

<p>然后用PEID 看看</p>

<p><img alt="" class="has" src="https://img-blog.csdnimg.cn/20190528204006103.jpg?x-oss-process=image/watermark,type_ZmFuZ3poZW5naGVpdGk,shadow_10,text_aHR0cHM6Ly9ibG9nLmNzZG4ubmV0L3dlaXhpbl80MjcyMTk1Nw==,size_16,color_FFFFFF,t_70"></p>

<p>所以.Net 反编译一下看看&nbsp; &nbsp; &nbsp;<a href="https://github.com/icsharpcode/ILSpy/releases" rel="nofollow" target="_blank">反编译工具</a></p>

<p><img alt="" class="has" height="640" src="https://img-blog.csdnimg.cn/20190528204033356.jpg?x-oss-process=image/watermark,type_ZmFuZ3poZW5naGVpdGk,shadow_10,text_aHR0cHM6Ly9ibG9nLmNzZG4ubmV0L3dlaXhpbl80MjcyMTk1Nw==,size_16,color_FFFFFF,t_70" width="866"></p>

<p>这里点开发现两个特殊的函数方法</p>

<p><img alt="" class="has" height="611" src="https://img-blog.csdnimg.cn/20190528204103172.jpg?x-oss-process=image/watermark,type_ZmFuZ3poZW5naGVpdGk,shadow_10,text_aHR0cHM6Ly9ibG9nLmNzZG4ubmV0L3dlaXhpbl80MjcyMTk1Nw==,size_16,color_FFFFFF,t_70" width="826"></p>

<p><img alt="" class="has" height="478" src="https://img-blog.csdnimg.cn/20190528204114569.jpg?x-oss-process=image/watermark,type_ZmFuZ3poZW5naGVpdGk,shadow_10,text_aHR0cHM6Ly9ibG9nLmNzZG4ubmV0L3dlaXhpbl80MjcyMTk1Nw==,size_16,color_FFFFFF,t_70" width="823"></p>

<p>从这里我们就发现了用户名和密码，再次登录得到了flag</p>

<p><img alt="" class="has" src="https://img-blog.csdnimg.cn/20190528204150601.jpg?x-oss-process=image/watermark,type_ZmFuZ3poZW5naGVpdGk,shadow_10,text_aHR0cHM6Ly9ibG9nLmNzZG4ubmV0L3dlaXhpbl80MjcyMTk1Nw==,size_16,color_FFFFFF,t_70"></p>

<p>&nbsp;</p>

<p>Web</p>

<p>1.</p>

<p><img alt="" class="has" height="277" src="https://img-blog.csdnimg.cn/20190502172141519.jpg?x-oss-process=image/watermark,type_ZmFuZ3poZW5naGVpdGk,shadow_10,text_aHR0cHM6Ly9ibG9nLmNzZG4ubmV0L3dlaXhpbl80MjcyMTk1Nw==,size_16,color_FFFFFF,t_70" width="751"></p>

<p>打开链接发现是一个登录界面。马上想到暴力破解。可是这里还有验证码，所以就很尴尬了</p>

<p><img alt="" class="has" src="https://img-blog.csdnimg.cn/20190502172241965.jpg?x-oss-process=image/watermark,type_ZmFuZ3poZW5naGVpdGk,shadow_10,text_aHR0cHM6Ly9ibG9nLmNzZG4ubmV0L3dlaXhpbl80MjcyMTk1Nw==,size_16,color_FFFFFF,t_70"></p>

<p>这里我找到了一个类似的比赛题目：<a href="https://blog.csdn.net/dongyanwen6036/article/details/77921407" rel="nofollow" target="_blank">https://blog.csdn.net/dongyanwen6036/article/details/77921407</a></p>

<p>里面提到发现&amp;vcode= 和PHPSESSID= 后面的数据删了就绕过了验证码（验证码存在SESSION中，后台校验验证码时未判断是否存在SESSION)</p>

<p>所以我想这里应该是类似的情况，所以祭出我的burpsuite吧</p>

<p><img alt="" class="has" height="384" src="https://img-blog.csdnimg.cn/20190502172449734.jpg?x-oss-process=image/watermark,type_ZmFuZ3poZW5naGVpdGk,shadow_10,text_aHR0cHM6Ly9ibG9nLmNzZG4ubmV0L3dlaXhpbl80MjcyMTk1Nw==,size_16,color_FFFFFF,t_70" width="571"></p>

<p>删除这里的两个数据，查看返回页面，居然确实是密码错误而不是验证码错误。事实证明暴力破解可行了</p>

<p><img alt="" class="has" height="278" src="https://img-blog.csdnimg.cn/20190502172556208.jpg?x-oss-process=image/watermark,type_ZmFuZ3poZW5naGVpdGk,shadow_10,text_aHR0cHM6Ly9ibG9nLmNzZG4ubmV0L3dlaXhpbl80MjcyMTk1Nw==,size_16,color_FFFFFF,t_70" width="837"></p>

<p>最坑爹最想不到的是数字密码居然是。。。996</p>

<p><img alt="" class="has" height="702" src="https://img-blog.csdnimg.cn/20190502172634542.jpg?x-oss-process=image/watermark,type_ZmFuZ3poZW5naGVpdGk,shadow_10,text_aHR0cHM6Ly9ibG9nLmNzZG4ubmV0L3dlaXhpbl80MjcyMTk1Nw==,size_16,color_FFFFFF,t_70" width="858"></p>

<p>果然程序员跟web狗最终都是要进ICU的啊！！！</p>

<p>2.</p>

<p><img alt="" class="has" height="323" src="https://img-blog.csdnimg.cn/2019050222572741.jpg?x-oss-process=image/watermark,type_ZmFuZ3poZW5naGVpdGk,shadow_10,text_aHR0cHM6Ly9ibG9nLmNzZG4ubmV0L3dlaXhpbl80MjcyMTk1Nw==,size_16,color_FFFFFF,t_70" width="868"></p>

<p>打开链接发现有php代码显示如下：</p>

<p><img alt="" class="has" height="443" src="https://img-blog.csdnimg.cn/20190502225810747.jpg?x-oss-process=image/watermark,type_ZmFuZ3poZW5naGVpdGk,shadow_10,text_aHR0cHM6Ly9ibG9nLmNzZG4ubmV0L3dlaXhpbl80MjcyMTk1Nw==,size_16,color_FFFFFF,t_70" width="873"></p>

<p>源代码：</p>

<pre class="has" name="code"><code class="hljs php"><ol class="hljs-ln" style="width:959px"><li><div class="hljs-ln-numbers"><div class="hljs-ln-line hljs-ln-n" data-line-number="1"></div></div><div class="hljs-ln-code"><div class="hljs-ln-line"><span class="hljs-meta">&lt;?php</span></div></div></li><li><div class="hljs-ln-numbers"><div class="hljs-ln-line hljs-ln-n" data-line-number="2"></div></div><div class="hljs-ln-code"><div class="hljs-ln-line">error_reporting(<span class="hljs-number">0</span>);</div></div></li><li><div class="hljs-ln-numbers"><div class="hljs-ln-line hljs-ln-n" data-line-number="3"></div></div><div class="hljs-ln-code"><div class="hljs-ln-line"><span class="hljs-keyword">require</span>&nbsp;<span class="hljs-string">'flag.php'</span>;</div></div></li><li><div class="hljs-ln-numbers"><div class="hljs-ln-line hljs-ln-n" data-line-number="4"></div></div><div class="hljs-ln-code"><div class="hljs-ln-line">$value&nbsp;=&nbsp;$_GET[<span class="hljs-string">'value'</span>];</div></div></li><li><div class="hljs-ln-numbers"><div class="hljs-ln-line hljs-ln-n" data-line-number="5"></div></div><div class="hljs-ln-code"><div class="hljs-ln-line">$password&nbsp;=&nbsp;$_GET[<span class="hljs-string">'password'</span>];</div></div></li><li><div class="hljs-ln-numbers"><div class="hljs-ln-line hljs-ln-n" data-line-number="6"></div></div><div class="hljs-ln-code"><div class="hljs-ln-line">$username&nbsp;=&nbsp;<span class="hljs-string">''</span>;</div></div></li><li><div class="hljs-ln-numbers"><div class="hljs-ln-line hljs-ln-n" data-line-number="7"></div></div><div class="hljs-ln-code"><div class="hljs-ln-line"> </div></div></li><li><div class="hljs-ln-numbers"><div class="hljs-ln-line hljs-ln-n" data-line-number="8"></div></div><div class="hljs-ln-code"><div class="hljs-ln-line"><span class="hljs-keyword">for</span>&nbsp;($i&nbsp;=&nbsp;<span class="hljs-number">0</span>;&nbsp;$i&nbsp;&lt;&nbsp;count($value);&nbsp;++$i)&nbsp;{</div></div></li><li><div class="hljs-ln-numbers"><div class="hljs-ln-line hljs-ln-n" data-line-number="9"></div></div><div class="hljs-ln-code"><div class="hljs-ln-line">&nbsp;&nbsp;&nbsp;&nbsp;<span class="hljs-keyword">if</span>&nbsp;($value[$i]&nbsp;&gt;&nbsp;<span class="hljs-number">32</span>&nbsp;&amp;&amp;&nbsp;$value[$i]&nbsp;&lt;&nbsp;<span class="hljs-number">127</span>)&nbsp;<span class="hljs-keyword">unset</span>($value);</div></div></li><li><div class="hljs-ln-numbers"><div class="hljs-ln-line hljs-ln-n" data-line-number="10"></div></div><div class="hljs-ln-code"><div class="hljs-ln-line">&nbsp;&nbsp;&nbsp;&nbsp;<span class="hljs-keyword">else</span>&nbsp;$username&nbsp;.=&nbsp;chr($value[$i]);</div></div></li><li><div class="hljs-ln-numbers"><div class="hljs-ln-line hljs-ln-n" data-line-number="11"></div></div><div class="hljs-ln-code"><div class="hljs-ln-line">&nbsp;&nbsp;&nbsp;&nbsp;<span class="hljs-keyword">if</span>&nbsp;($username&nbsp;==&nbsp;<span class="hljs-string">'w3lc0me_To_ISCC2019'</span>&nbsp;&amp;&amp;&nbsp;intval($password)&nbsp;&lt;&nbsp;<span class="hljs-number">2333</span>&nbsp;&amp;&amp;&nbsp;intval($password&nbsp;+&nbsp;<span class="hljs-number">1</span>)&nbsp;&gt;&nbsp;<span class="hljs-number">2333</span>)&nbsp;{</div></div></li><li><div class="hljs-ln-numbers"><div class="hljs-ln-line hljs-ln-n" data-line-number="12"></div></div><div class="hljs-ln-code"><div class="hljs-ln-line">&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;<span class="hljs-keyword">echo</span>&nbsp;<span class="hljs-string">'Hello&nbsp;'</span>.$username.<span class="hljs-string">'!'</span>,&nbsp;<span class="hljs-string">'&lt;br&gt;'</span>,&nbsp;PHP_EOL;</div></div></li><li><div class="hljs-ln-numbers"><div class="hljs-ln-line hljs-ln-n" data-line-number="13"></div></div><div class="hljs-ln-code"><div class="hljs-ln-line">&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;<span class="hljs-keyword">echo</span>&nbsp;$flag,&nbsp;<span class="hljs-string">'&lt;hr&gt;'</span>;</div></div></li><li><div class="hljs-ln-numbers"><div class="hljs-ln-line hljs-ln-n" data-line-number="14"></div></div><div class="hljs-ln-code"><div class="hljs-ln-line">&nbsp;&nbsp;&nbsp;&nbsp;}</div></div></li><li><div class="hljs-ln-numbers"><div class="hljs-ln-line hljs-ln-n" data-line-number="15"></div></div><div class="hljs-ln-code"><div class="hljs-ln-line">}</div></div></li><li><div class="hljs-ln-numbers"><div class="hljs-ln-line hljs-ln-n" data-line-number="16"></div></div><div class="hljs-ln-code"><div class="hljs-ln-line"> </div></div></li><li><div class="hljs-ln-numbers"><div class="hljs-ln-line hljs-ln-n" data-line-number="17"></div></div><div class="hljs-ln-code"><div class="hljs-ln-line">highlight_file(<span class="hljs-keyword">__FILE__</span>);</div></div></li><li><div class="hljs-ln-numbers"><div class="hljs-ln-line hljs-ln-n" data-line-number="18"></div></div><div class="hljs-ln-code"><div class="hljs-ln-line"> </div></div></li></ol></code><div class="hljs-button {2}" data-title="复制" onclick="hljs.copyCode(event)"></div></pre>

<p>&nbsp;</p>

<p>大概意思就是包含了flag.php文件，然后有三个参数，其中value参数的值不能在32到127中间，也就是不能直接用ascll码代替。然后password参数用了intval()方法后要满足两个条件就得到flag。</p>

<p>这里有两个技巧：</p>

<p>（1）chr函数在转换时会自动取模256,所以我们只需要在原本ascii码基础上+256即可</p>

<p>（2）intval()在处理16进制时存在问题,但强制转换时时正常的</p>

<p>所以这个题的payload是：http://39.100.83.188:8001/index.php？value[]=375&amp;value[]=307&amp;value[]=364&amp;value[]=355&amp;value[]=304&amp;value[]=365&amp;value[]=357&amp;value[]=351&amp;value[]=340&amp;value[]=367&amp;value[]=351&amp;value[]=329&amp;value[]=339&amp;value[]=323&amp;value[]=323&amp;value[]=306&amp;value[]=304&amp;value[]=305&amp;value[]=313&amp;password=2332e1</p>

<p><img alt="" class="has" height="96" src="https://img-blog.csdnimg.cn/20190502230445433.jpg?x-oss-process=image/watermark,type_ZmFuZ3poZW5naGVpdGk,shadow_10,text_aHR0cHM6Ly9ibG9nLmNzZG4ubmV0L3dlaXhpbl80MjcyMTk1Nw==,size_16,color_FFFFFF,t_70" width="894"></p>

<p><img alt="" class="has" height="349" src="https://img-blog.csdnimg.cn/2019050223050027.jpg?x-oss-process=image/watermark,type_ZmFuZ3poZW5naGVpdGk,shadow_10,text_aHR0cHM6Ly9ibG9nLmNzZG4ubmV0L3dlaXhpbl80MjcyMTk1Nw==,size_16,color_FFFFFF,t_70" width="883"></p>

<p>3.</p>

<p><img alt="" class="has" height="303" src="https://img-blog.csdnimg.cn/20190528162638888.jpg?x-oss-process=image/watermark,type_ZmFuZ3poZW5naGVpdGk,shadow_10,text_aHR0cHM6Ly9ibG9nLmNzZG4ubmV0L3dlaXhpbl80MjcyMTk1Nw==,size_16,color_FFFFFF,t_70" width="817"></p>

<p>打开链接发现php源码如下：</p>

<p><img alt="" class="has" src="https://img-blog.csdnimg.cn/20190528162713122.jpg?x-oss-process=image/watermark,type_ZmFuZ3poZW5naGVpdGk,shadow_10,text_aHR0cHM6Ly9ibG9nLmNzZG4ubmV0L3dlaXhpbl80MjcyMTk1Nw==,size_16,color_FFFFFF,t_70"></p>

<p>源代码：</p>

<pre class="has" name="code"><code class="hljs xml"><ol class="hljs-ln" style="width:765px"><li><div class="hljs-ln-numbers"><div class="hljs-ln-line hljs-ln-n" data-line-number="1"></div></div><div class="hljs-ln-code"><div class="hljs-ln-line"><span class="php"><span class="hljs-meta">&lt;?php</span> </span></div></div></li><li><div class="hljs-ln-numbers"><div class="hljs-ln-line hljs-ln-n" data-line-number="2"></div></div><div class="hljs-ln-code"><div class="hljs-ln-line">error_reporting(<span class="hljs-number">0</span>); </div></div></li><li><div class="hljs-ln-numbers"><div class="hljs-ln-line hljs-ln-n" data-line-number="3"></div></div><div class="hljs-ln-code"><div class="hljs-ln-line"><span class="hljs-keyword">include</span>(<span class="hljs-string">"flag.php"</span>); </div></div></li><li><div class="hljs-ln-numbers"><div class="hljs-ln-line hljs-ln-n" data-line-number="4"></div></div><div class="hljs-ln-code"><div class="hljs-ln-line">$hashed_key = <span class="hljs-string">'ddbafb4eb89e218701472d3f6c087fdf7119dfdd560f9d1fcbe7482b0feea05a'</span>; </div></div></li><li><div class="hljs-ln-numbers"><div class="hljs-ln-line hljs-ln-n" data-line-number="5"></div></div><div class="hljs-ln-code"><div class="hljs-ln-line">$parsed = parse_url($_SERVER[<span class="hljs-string">'REQUEST_URI'</span>]); </div></div></li><li><div class="hljs-ln-numbers"><div class="hljs-ln-line hljs-ln-n" data-line-number="6"></div></div><div class="hljs-ln-code"><div class="hljs-ln-line"><span class="hljs-keyword">if</span>(<span class="hljs-keyword">isset</span>($parsed[<span class="hljs-string">"query"</span>])){ </div></div></li><li><div class="hljs-ln-numbers"><div class="hljs-ln-line hljs-ln-n" data-line-number="7"></div></div><div class="hljs-ln-code"><div class="hljs-ln-line">    $query = $parsed[<span class="hljs-string">"query"</span>]; </div></div></li><li><div class="hljs-ln-numbers"><div class="hljs-ln-line hljs-ln-n" data-line-number="8"></div></div><div class="hljs-ln-code"><div class="hljs-ln-line">    $parsed_query = parse_str($query); </div></div></li><li><div class="hljs-ln-numbers"><div class="hljs-ln-line hljs-ln-n" data-line-number="9"></div></div><div class="hljs-ln-code"><div class="hljs-ln-line">    <span class="hljs-keyword">if</span>($parsed_query!=<span class="hljs-keyword">NULL</span>){ </div></div></li><li><div class="hljs-ln-numbers"><div class="hljs-ln-line hljs-ln-n" data-line-number="10"></div></div><div class="hljs-ln-code"><div class="hljs-ln-line">        $action = $parsed_query[<span class="hljs-string">'action'</span>]; </div></div></li><li><div class="hljs-ln-numbers"><div class="hljs-ln-line hljs-ln-n" data-line-number="11"></div></div><div class="hljs-ln-code"><div class="hljs-ln-line">    } </div></div></li><li><div class="hljs-ln-numbers"><div class="hljs-ln-line hljs-ln-n" data-line-number="12"></div></div><div class="hljs-ln-code"><div class="hljs-ln-line"> </div></div></li><li><div class="hljs-ln-numbers"><div class="hljs-ln-line hljs-ln-n" data-line-number="13"></div></div><div class="hljs-ln-code"><div class="hljs-ln-line">    <span class="hljs-keyword">if</span>($action===<span class="hljs-string">"auth"</span>){ </div></div></li><li><div class="hljs-ln-numbers"><div class="hljs-ln-line hljs-ln-n" data-line-number="14"></div></div><div class="hljs-ln-code"><div class="hljs-ln-line">        $key = $_GET[<span class="hljs-string">"key"</span>]; </div></div></li><li><div class="hljs-ln-numbers"><div class="hljs-ln-line hljs-ln-n" data-line-number="15"></div></div><div class="hljs-ln-code"><div class="hljs-ln-line">        $hashed_input = hash(<span class="hljs-string">'sha256'</span>, $key); </div></div></li><li><div class="hljs-ln-numbers"><div class="hljs-ln-line hljs-ln-n" data-line-number="16"></div></div><div class="hljs-ln-code"><div class="hljs-ln-line">        <span class="hljs-keyword">if</span>($hashed_input!==$hashed_key){ </div></div></li><li><div class="hljs-ln-numbers"><div class="hljs-ln-line hljs-ln-n" data-line-number="17"></div></div><div class="hljs-ln-code"><div class="hljs-ln-line">            <span class="hljs-keyword">die</span>(<span class="hljs-string">"&lt;img src='cxk.jpg'&gt;"</span>); </div></div></li><li><div class="hljs-ln-numbers"><div class="hljs-ln-line hljs-ln-n" data-line-number="18"></div></div><div class="hljs-ln-code"><div class="hljs-ln-line">        } </div></div></li><li><div class="hljs-ln-numbers"><div class="hljs-ln-line hljs-ln-n" data-line-number="19"></div></div><div class="hljs-ln-code"><div class="hljs-ln-line"> </div></div></li><li><div class="hljs-ln-numbers"><div class="hljs-ln-line hljs-ln-n" data-line-number="20"></div></div><div class="hljs-ln-code"><div class="hljs-ln-line">        <span class="hljs-keyword">echo</span> $flag; </div></div></li><li><div class="hljs-ln-numbers"><div class="hljs-ln-line hljs-ln-n" data-line-number="21"></div></div><div class="hljs-ln-code"><div class="hljs-ln-line">    } </div></div></li><li><div class="hljs-ln-numbers"><div class="hljs-ln-line hljs-ln-n" data-line-number="22"></div></div><div class="hljs-ln-code"><div class="hljs-ln-line">}<span class="hljs-keyword">else</span>{ </div></div></li><li><div class="hljs-ln-numbers"><div class="hljs-ln-line hljs-ln-n" data-line-number="23"></div></div><div class="hljs-ln-code"><div class="hljs-ln-line">    show_source(<span class="hljs-keyword">__FILE__</span>); </div></div></li><li><div class="hljs-ln-numbers"><div class="hljs-ln-line hljs-ln-n" data-line-number="24"></div></div><div class="hljs-ln-code"><div class="hljs-ln-line">}<span class="hljs-meta">?&gt;</span></div></div></li></ol></code><div class="hljs-button {2}" data-title="复制" onclick="hljs.copyCode(event)"></div></pre>

<p>&nbsp;</p>

<p>这里简单审计一下，大概意思就是当发现传入的参数中 action 为 auth，并且 key 和 hashed_key 的值相等时，就给出 flag。</p>

<p>这里可以用到一个非常危险的函数 parse_str，具体情况请看&nbsp;<a href="https://www.php.net/manual/zh/function.parse-str.php" rel="nofollow" target="_blank">https://www.php.net/manual/zh/function.parse-str.php</a></p>

<p>如果传入的是 query_string（形如first=value&amp;arr[]=foo+bar&amp;arr[]=baz ），那么就会将其解析为变量（设置变量 first=value, arr[0]=foo&nbsp;bar，arr[1]=baz）</p>

<p>所以利用这一漏洞，我们就可以实现变量覆盖了，直接将 hashed_key 覆盖为我们想要的值即可。这里我选择覆盖 sha256(“swzaq”) = 07e599430c991fd44f41e7658b8816143ba7ce316c3a503291bacc82f1b569ee</p>

<p><img alt="" class="has" src="https://img-blog.csdnimg.cn/2019052816342388.jpg?x-oss-process=image/watermark,type_ZmFuZ3poZW5naGVpdGk,shadow_10,text_aHR0cHM6Ly9ibG9nLmNzZG4ubmV0L3dlaXhpbl80MjcyMTk1Nw==,size_16,color_FFFFFF,t_70"></p>

<p>payload 如下：&nbsp;</p>

<pre class="has" name="code"><code class="hljs vbnet">/?action=auth&amp;<span class="hljs-keyword">key</span>=swzaq&amp;hashed_key=<span class="hljs-number">07e599430</span>c991fd44f41e7658b8816143ba7ce316c3a503291bacc82f1b569ee</code><div class="hljs-button {2}" data-title="复制" onclick="hljs.copyCode(event)"></div></pre>

<p><img alt="" class="has" src="https://img-blog.csdnimg.cn/20190528163521369.jpg?x-oss-process=image/watermark,type_ZmFuZ3poZW5naGVpdGk,shadow_10,text_aHR0cHM6Ly9ibG9nLmNzZG4ubmV0L3dlaXhpbl80MjcyMTk1Nw==,size_16,color_FFFFFF,t_70"></p>

<p>&nbsp;</p>
          </div>
                  </div>
