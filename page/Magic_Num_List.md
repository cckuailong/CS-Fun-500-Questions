# 文件幻数列表

## 前言

Magic number，即幻数，它可以用来标记文件或者协议的格式，很多文件都有幻数标志来表明该文件的格式。

一些操作系统使用幻数识别进行文件类型识别，如 AmigaOS。

列表取自 [wiki](https://en.wikipedia.org/wiki/List_of_file_signatures)

## 幻数列表

<table>
  <thead>
    <tr>
      <th>Hex signature</th>
      <th>ISO 8859-1</th>
      <th>Offset</th>
      <th>Filename extension</th>
      <th>Description</th></tr>
  </thead>
  <tbody>
    <tr>
      <td>
        <pre>23 21</pre></td>
      <td>
        <pre>#!</pre></td>
      <td>0</td>
      <td></td>
      <td>shebang (#!).</td></tr>
    <tr>
      <td>
        <pre>a1 b2 c3 d4</pre>
        <pre>d4 c3 b2 a1</pre></td>
      <td>
        <pre>¡²ÃÔ</pre>
        <pre>ÔÃ²¡</pre></td>
      <td>0</td>
      <td>pcap</td>
      <td>Libpcap File Format</td></tr>
    <tr>
      <td>
        <pre>0a 0d 0d 0a</pre></td>
      <td>
        <pre>....</pre></td>
      <td>0</td>
      <td>pcapng</td>
      <td>PCAP Next Generation Dump File Format</td></tr>
    <tr>
      <td>
        <pre>ed ab ee db</pre></td>
      <td>
        <pre>í«îÛ</pre></td>
      <td>0</td>
      <td>rpm</td>
      <td>RedHat Package Manager (RPM) package</td></tr>
    <tr>
      <td>
        <pre>53 51 4c 69 74 65 <br>20 66 6f 72 6d 61 <br>74 20 33 00</pre></td>
      <td>
        <pre>SQLite format 3.</pre></td>
      <td>0</td>
      <td>sqlitedb
        <br>sqlite
        <br>db</td>
      <td>SQLite Database</td></tr>
    <tr>
      <td>
        <pre>53 50 30 31</pre></td>
      <td>
        <pre>SP01</pre></td>
      <td>0</td>
      <td>bin</td>
      <td>Amazon Kindle Update Package</td></tr>
    <tr>
      <td>
        <pre>00</pre></td>
      <td>
        <pre>.</pre></td>
      <td>0</td>
      <td>PIC
        <br>PIF
        <br>SEA
        <br>YTR</td>
      <td>IBM Storyboard bitmap file
        <br>
        <p>Windows Program Information File
          <br>Mac Stuffit Self-Extracting Archive
          <br>IRIS OCR data file</p></td>
    </tr>
    <tr>
      <td>
        <pre>00 00 00 00 00 00 <br>00 00 00 00 00 00 <br>00 00 00 00 00 00 <br>00 00 00 00 00 00</pre></td>
      <td>
        <pre>........ ........ ........</pre></td>
      <td>11</td>
      <td>PDB</td>
      <td>PalmPilot Database/Document File</td></tr>
    <tr>
      <td>
        <pre>BE BA FE CA</pre></td>
      <td>
        <pre>¾ºþÊ</pre></td>
      <td>0</td>
      <td>DBA</td>
      <td>Palm Desktop Calendar Archive</td></tr>
    <tr>
      <td>
        <pre>00 01 42 44</pre></td>
      <td>
        <pre>..BD</pre></td>
      <td>0</td>
      <td>DBA</td>
      <td>Palm Desktop To Do Archive</td></tr>
    <tr>
      <td>
        <pre>00 01 44 54</pre></td>
      <td>
        <pre>..DT</pre></td>
      <td>0</td>
      <td>TDA</td>
      <td>Palm Desktop Calendar Archive</td></tr>
    <tr>
      <td>
        <pre>54 44 46 24</pre></td>
      <td>
        <pre>TDF$</pre></td>
      <td>0</td>
      <td>TDF$</td>
      <td>Telegram Desktop File</td></tr>
    <tr>
      <td>
        <pre>54 44 45 46</pre></td>
      <td>
        <pre>TDEF</pre></td>
      <td>0</td>
      <td>TDEF</td>
      <td>Telegram Desktop Encrypted File</td></tr>
    <tr>
      <td>
        <pre>00 01 00 00</pre></td>
      <td>
        <pre>....</pre></td>
      <td>0</td>
      <td></td>
      <td>Palm Desktop Data File (Access format)</td></tr>
    <tr>
      <td>
        <pre>00 00 01 00</pre></td>
      <td>
        <pre>....</pre></td>
      <td>0</td>
      <td>ico</td>
      <td>Computer icon encoded in ICO file format</td></tr>
    <tr>
      <td>
        <pre>66 74 79 70 33 67</pre></td>
      <td>
        <pre>ftyp3g</pre></td>
      <td>4</td>
      <td>3gp
        <br>3g2</td>
      <td>3rd Generation Partnership Project 3GPP and 3GPP2 multimedia files</td></tr>
    <tr>
      <td>
        <pre>1F 9D</pre></td>
      <td>
        <pre>..</pre></td>
      <td>0</td>
      <td>z
        <br>tar.z</td>
      <td>compressed file (often tar zip)
        <br>
        <p>using Lempel-Ziv-Welch algorithm</p>
      </td>
    </tr>
    <tr>
      <td>
        <pre>1F A0</pre></td>
      <td>
        <pre>.&nbsp;</pre></td>
      <td>0</td>
      <td>z
        <br>tar.z</td>
      <td>Compressed file (often tar zip)
        <br>
        <p>using LZH algorithm</p>
      </td>
    </tr>
    <tr>
      <td>
        <pre>42 41 43 4B 4D 49 <br>4B 45 44 49 53 4B</pre></td>
      <td>
        <pre>BACKMIKE DISK</pre></td>
      <td>0</td>
      <td>bac</td>
      <td>File or tape containing a backup done with AmiBack on an Amiga.
        <p>It typically is paired with an index file (idx) with the table of contents.</p>
      </td>
    </tr>
    <tr>
      <td>
        <pre>42 5A 68</pre></td>
      <td>
        <pre>BZh</pre></td>
      <td>0</td>
      <td>bz2</td>
      <td>Compressed file using Bzip2 algorithm</td></tr>
    <tr>
      <td>
        <pre>47 49 46 38 37 61</pre>
        <pre>47 49 46 38 39 61</pre></td>
      <td>
        <pre>GIF87a</pre>
        <pre>GIF89a</pre></td>
      <td>0</td>
      <td>gif</td>
      <td>Image file encoded in the Graphics Interchange Format (GIF)</td></tr>
    <tr>
      <td>
        <pre>49 49 2A 00</pre>(little endian format)
        <br>
        <pre>4D 4D 00 2A</pre>(big endian format)</td>
      <td>
        <pre>II*.</pre>
        <pre>MM.*</pre></td>
      <td>0</td>
      <td>tif
        <br>tiff</td>
      <td>Tagged Image File Format</td></tr>
    <tr>
      <td>
        <pre>49 49 2A 00 10 00 <br>00 00 43 52</pre></td>
      <td>
        <pre>II*..... CR</pre></td>
      <td>0</td>
      <td>cr2</td>
      <td>Canon RAW Format Version 2
        <br>Canon's RAW format is based on the TIFF file format</td></tr>
    <tr>
      <td>
        <pre>80 2A 5F D7</pre></td>
      <td>
        <pre>.*_.</pre></td>
      <td>0</td>
      <td>cin</td>
      <td>Kodak Cineon image</td></tr>
    <tr>
      <td>
        <pre>52 4E 43 01</pre>
        <pre>52 4E 43 02</pre></td>
      <td>
        <pre>RNC.</pre></td>
      <td>0</td>
      <td></td>
      <td>Compressed file using Rob Northen Compression (version 1 and 2) algorithm</td></tr>
    <tr>
      <td>
        <pre>53 44 50 58</pre>(big endian format)
        <br>
        <pre>58 50 44 53</pre>(little endian format)</td>
      <td>
        <pre>SDPX</pre>
        <pre>XPDS</pre></td>
      <td>0</td>
      <td>dpx</td>
      <td>SMPTE DPX image</td></tr>
    <tr>
      <td>
        <pre>76 2F 31 01</pre></td>
      <td>
        <pre>v/1.</pre></td>
      <td>0</td>
      <td>exr</td>
      <td>OpenEXR image</td></tr>
    <tr>
      <td>
        <pre>42 50 47 FB</pre></td>
      <td>
        <pre>BPGû</pre></td>
      <td>0</td>
      <td>bpg</td>
      <td>Better Portable Graphics format</td></tr>
    <tr>
      <td>
        <pre>FF D8 FF DB</pre>
        <pre>FF D8 FF E0 00 10 <br>4A 46 49 46 00 01</pre>
        <pre>FF D8 FF EE</pre>
        <pre>FF D8 FF <br>E1&nbsp;??&nbsp;?? <br>45 78 69 66 00 00</pre></td>
      <td>
        <pre>ÿØÿÛ</pre>
        <pre>ÿØÿà..JFIF..</pre>
        <pre>ÿØÿî</pre>
        <pre>ÿØÿá..Exif..</pre></td>
      <td>0</td>
      <td>jpg
        <br>jpeg</td>
      <td>JPEG raw or in the JFIF or Exif file format</td></tr>
    <tr>
      <td>
        <pre>46 4F 52 <br>4D&nbsp;??&nbsp;??&nbsp;??&nbsp;?? <br>49 4C 42 4D</pre></td>
      <td>
        <pre>FORM.... ILBM</pre></td>
      <td>0
        <p>any</p>
      </td>
      <td>ilbm
        <br>lbm
        <br>ibm
        <br>iff</td>
      <td>IFF Interleaved Bitmap Image</td></tr>
    <tr>
      <td>
        <pre>46 4F 52 <br>4D&nbsp;??&nbsp;??&nbsp;??&nbsp;?? <br>38 53 56 58</pre></td>
      <td>
        <pre>FORM.... 8SVX</pre></td>
      <td>0
        <p>any</p>
      </td>
      <td>8svx
        <br>8sv
        <br>svx
        <br>snd
        <br>iff</td>
      <td>IFF 8-Bit Sampled Voice</td></tr>
    <tr>
      <td>
        <pre>46 4F 52 <br>4D&nbsp;??&nbsp;??&nbsp;??&nbsp;?? <br>41 43 42 4D</pre></td>
      <td>
        <pre>FORM.... ACBM</pre></td>
      <td>0
        <p>any</p>
      </td>
      <td>acbm
        <br>iff</td>
      <td>Amiga Contiguous Bitmap</td></tr>
    <tr>
      <td>
        <pre>46 4F 52 <br>4D&nbsp;??&nbsp;??&nbsp;??&nbsp;?? <br>41 4E 42 4D</pre></td>
      <td>
        <pre>FORM.... ANBM</pre></td>
      <td>0
        <p>any</p>
      </td>
      <td>anbm
        <br>iff</td>
      <td>IFF Animated Bitmap</td></tr>
    <tr>
      <td>
        <pre>46 4F 52 <br>4D&nbsp;??&nbsp;??&nbsp;??&nbsp;?? <br>41 4E 49 4D</pre></td>
      <td>
        <pre>FORM.... ANIM</pre></td>
      <td>0
        <p>any</p>
      </td>
      <td>anim
        <br>iff</td>
      <td>IFF CEL Animation</td></tr>
    <tr>
      <td>
        <pre>46 4F 52 <br>4D&nbsp;??&nbsp;??&nbsp;??&nbsp;?? <br>46 41 58 58</pre></td>
      <td>
        <pre>FORM.... FAXX</pre></td>
      <td>0
        <p>any</p>
      </td>
      <td>faxx
        <br>fax
        <br>iff</td>
      <td>IFF Facsimile Image</td></tr>
    <tr>
      <td>
        <pre>46 4F 52 <br>4D&nbsp;??&nbsp;??&nbsp;??&nbsp;?? <br>46 54 58 54</pre></td>
      <td>
        <pre>FORM.... FTXT</pre></td>
      <td>0
        <p>any</p>
      </td>
      <td>ftxt
        <br>iff</td>
      <td>IFF Formatted Text</td></tr>
    <tr>
      <td>
        <pre>46 4F 52 <br>4D&nbsp;??&nbsp;??&nbsp;??&nbsp;?? <br>53 4D 55 53</pre></td>
      <td>
        <pre>FORM.... SMUS</pre></td>
      <td>0
        <p>any</p>
      </td>
      <td>smus
        <br>smu
        <br>mus
        <br>iff</td>
      <td>IFF Simple Musical Score</td></tr>
    <tr>
      <td>
        <pre>46 4F 52 <br>4D&nbsp;??&nbsp;??&nbsp;??&nbsp;?? <br>43 4D 55 53</pre></td>
      <td>
        <pre>FORM.... CMUS</pre></td>
      <td>0
        <p>any</p>
      </td>
      <td>cmus
        <br>mus
        <br>iff</td>
      <td>IFF Musical Score</td></tr>
    <tr>
      <td>
        <pre>46 4F 52 <br>4D&nbsp;??&nbsp;??&nbsp;??&nbsp;?? <br>59 55 56 4E</pre></td>
      <td>
        <pre>FORM.... YUVN</pre></td>
      <td>0
        <p>any</p>
      </td>
      <td>yuvn
        <br>yuv
        <br>iff</td>
      <td>IFF YUV Image</td></tr>
    <tr>
      <td>
        <pre>46 4F 52 <br>4D&nbsp;??&nbsp;??&nbsp;??&nbsp;?? <br>46 41 4E 54</pre></td>
      <td>
        <pre>FORM.... FANT</pre></td>
      <td>0
        <p>any</p>
      </td>
      <td>iff</td>
      <td>Amiga Fantavision Movie</td></tr>
    <tr>
      <td>
        <pre>46 4F 52 <br>4D&nbsp;??&nbsp;??&nbsp;??&nbsp;?? <br>41 49 46 46</pre></td>
      <td>
        <pre>FORM.... AIFF</pre></td>
      <td>0
        <p>any</p>
      </td>
      <td>aiff
        <br>aif
        <br>aifc
        <br>snd
        <br>iff</td>
      <td>Audio Interchange File Format</td></tr>
    <tr>
      <td>
        <pre>49 4E 44 58</pre></td>
      <td>
        <pre>INDX</pre></td>
      <td>0</td>
      <td>idx</td>
      <td>Index file to a file or tape containing a backup done with AmiBack on an Amiga.</td></tr>
    <tr>
      <td>
        <pre>4C 5A 49 50</pre></td>
      <td>
        <pre>LZIP</pre></td>
      <td>0</td>
      <td>lz</td>
      <td>lzip compressed file</td></tr>
    <tr>
      <td>
        <pre>4D 5A</pre></td>
      <td>
        <pre>MZ</pre></td>
      <td>0</td>
      <td>exe
        <br>dll</td>
      <td>DOS MZ executable file format and its descendants (including NE and PE)</td></tr>
    <tr>
      <td>
        <pre>50 4B 03 04</pre>
        <br>
        <pre>50 4B 05 06</pre>(empty archive)
        <br>
        <pre>50 4B 07 08</pre>(spanned archive)</td>
      <td>
        <pre>PK..</pre></td>
      <td>0</td>
      <td>zip
        <br>aar
        <br>apk
        <br>docx
        <br>epub
        <br>ipa
        <br>jar
        <br>kmz
        <br>maff
        <br>odp
        <br>ods
        <br>odt
        <br>pk3
        <br>pk4
        <br>pptx
        <br>usdz
        <br>vsdx
        <br>xlsx
        <br>xpi</td>
      <td>zip file format and formats based on it, such as EPUB, JAR, ODF, OOXML</td></tr>
    <tr>
      <td>
        <pre>52 61 72 21 1A 07 <br>00</pre></td>
      <td>
        <pre>Rar!...</pre>
        <br></td>
      <td>0</td>
      <td>rar</td>
      <td>RAR archive version 1.50 onwards</td></tr>
    <tr>
      <td>
        <pre>52 61 72 21 1A 07 <br>01 00</pre></td>
      <td>
        <pre>Rar!....</pre></td>
      <td>0</td>
      <td>rar</td>
      <td>RAR archive version 5.0 onwards</td></tr>
    <tr>
      <td>
        <pre>7F 45 4C 46</pre></td>
      <td>
        <pre>.ELF</pre></td>
      <td>0</td>
      <td></td>
      <td>Executable and Linkable Format</td></tr>
    <tr>
      <td>
        <pre>89 50 4E 47 0D 0A <br>1A 0A</pre></td>
      <td>
        <pre>.PNG....</pre></td>
      <td>0</td>
      <td>png</td>
      <td>Image encoded in the Portable Network Graphics format</td></tr>
    <tr>
      <td>
        <pre>CA FE BA BE</pre></td>
      <td>
        <pre>Êþº¾</pre></td>
      <td>0</td>
      <td>class</td>
      <td>Java class file, Mach-O Fat Binary</td></tr>
    <tr>
      <td>
        <pre>EF BB BF</pre></td>
      <td>
        <pre>ï»¿</pre></td>
      <td>0</td>
      <td></td>
      <td>UTF-8 encoded Unicode byte order mark, commonly seen in text files.</td></tr>
    <tr>
      <td>
        <pre>FE ED FA CE</pre></td>
      <td>
        <pre>........</pre></td>
      <td>0
        <p>0x1000</p>
      </td>
      <td></td>
      <td>Mach-O binary (32-bit)</td></tr>
    <tr>
      <td>
        <pre>FE ED FA CF</pre></td>
      <td>
        <pre>........</pre></td>
      <td>0
        <p>0x1000</p>
      </td>
      <td></td>
      <td>Mach-O binary (64-bit)</td></tr>
    <tr>
      <td>
        <pre>FE ED FE ED</pre></td>
      <td>
        <pre>þíþí</pre></td>
      <td>0</td>
      <td></td>
      <td>JKS JavakeyStore</td></tr>
    <tr>
      <td>
        <pre>CE FA ED FE</pre></td>
      <td>
        <pre>........</pre></td>
      <td>0</td>
      <td></td>
      <td>Mach-O binary (reverse byte ordering scheme, 32-bit)</td></tr>
    <tr>
      <td>
        <pre>CF FA ED FE</pre></td>
      <td>
        <pre>........</pre></td>
      <td>0</td>
      <td></td>
      <td>Mach-O binary (reverse byte ordering scheme, 64-bit)</td></tr>
    <tr>
      <td>
        <pre>FF FE</pre></td>
      <td>
        <pre>..</pre></td>
      <td>0</td>
      <td></td>
      <td>Byte-order mark for text file encoded in little-endian 16-bit Unicode Transfer Format</td></tr>
    <tr>
      <td>
        <pre>FF FE 00 00</pre></td>
      <td>
        <pre>....</pre></td>
      <td>0</td>
      <td></td>
      <td>Byte-order mark for text file encoded in little-endian 32-bit Unicode Transfer Format</td></tr>
    <tr>
      <td>
        <pre>25 21 50 53</pre></td>
      <td>
        <pre>%!PS</pre></td>
      <td>0</td>
      <td>ps</td>
      <td>PostScript document</td></tr>
    <tr>
      <td>
        <pre>25 50 44 46 2d</pre></td>
      <td>
        <pre>%PDF-</pre></td>
      <td>0</td>
      <td>pdf</td>
      <td>PDF document</td></tr>
    <tr>
      <td>
        <pre>30 26 B2 75 8E 66 <br>CF 11 A6 D9 00 AA <br>00 62 CE 6C</pre></td>
      <td>
        <pre>0&amp;²u.fÏ .¦Ù.ª.bÎl</pre></td>
      <td>0</td>
      <td>asf
        <br>wma
        <br>wmv</td>
      <td>Advanced Systems Format</td></tr>
    <tr>
      <td>
        <pre>24 53 44 49 30 30 <br>30 31</pre></td>
      <td>
        <pre>$SDI0001</pre></td>
      <td>0</td>
      <td></td>
      <td>System Deployment Image, a disk image format used by Microsoft</td></tr>
    <tr>
      <td>
        <pre>4F 67 67 53</pre></td>
      <td>
        <pre>OggS</pre></td>
      <td>0</td>
      <td>ogg
        <br>oga
        <br>ogv</td>
      <td>Ogg, an open source media container format</td></tr>
    <tr>
      <td>
        <pre>38 42 50 53</pre></td>
      <td>
        <pre>8BPS</pre></td>
      <td>0</td>
      <td>psd</td>
      <td>Photoshop Document file, Adobe Photoshop's native file format</td></tr>
    <tr>
      <td>
        <pre>52 49 46 <br>46&nbsp;??&nbsp;??&nbsp;??&nbsp;?? <br>57 41 56 45</pre></td>
      <td>
        <pre>RIFF.... WAVE</pre></td>
      <td>0</td>
      <td>wav</td>
      <td>Waveform Audio File Format</td></tr>
    <tr>
      <td>
        <pre>52 49 46 <br>46&nbsp;??&nbsp;??&nbsp;??&nbsp;?? <br>41 56 49 20</pre></td>
      <td>
        <pre>RIFF.... AVI.</pre></td>
      <td>0</td>
      <td>avi</td>
      <td>Audio Video Interleave video format</td></tr>
    <tr>
      <td>
        <pre>FF FB</pre></td>
      <td>
        <pre>ÿû</pre></td>
      <td>0</td>
      <td>mp3</td>
      <td>MPEG-1 Layer 3 file without an ID3 tag or with an ID3v1 tag (which's appended at the end of the file)</td></tr>
    <tr>
      <td>
        <pre>49 44 33</pre></td>
      <td>
        <pre>ID3</pre></td>
      <td>0</td>
      <td>mp3</td>
      <td>MP3 file with an ID3v2 container</td></tr>
    <tr>
      <td>
        <pre>42 4D</pre></td>
      <td>
        <pre>BM</pre></td>
      <td>0</td>
      <td>bmp
        <br>dib</td>
      <td>BMP file, a bitmap format used mostly in the Windows world</td></tr>
    <tr>
      <td>
        <pre>43 44 30 30 31</pre></td>
      <td>
        <pre>CD001</pre></td>
      <td>0x8001
        <br>
        <p>0x8801
          <br>0x9001</p></td>
      <td>iso</td>
      <td>ISO9660 CD/DVD image file</td></tr>
    <tr>
      <td>
        <pre>53 49 4D 50 4C 45 <br>20 20</pre>
        <pre>3D 20 20 20 20 20 <br>20 20 20 20 20 20 <br>20 20 20 20 20 20 <br>20 20 20 54</pre></td>
      <td>
        <pre>SIMPLE = T</pre></td>
      <td>0</td>
      <td>fits</td>
      <td>Flexible Image Transport System (FITS)</td></tr>
    <tr>
      <td>
        <pre>66 4C 61 43</pre></td>
      <td>
        <pre>fLaC</pre></td>
      <td>0</td>
      <td>flac</td>
      <td>Free Lossless Audio Codec</td></tr>
    <tr>
      <td>
        <pre>4D 54 68 64</pre></td>
      <td>
        <pre>MThd</pre></td>
      <td>0</td>
      <td>mid
        <br>midi</td>
      <td>MIDI sound file</td></tr>
    <tr>
      <td>
        <pre>D0 CF 11 E0 A1 B1 <br>1A E1</pre></td>
      <td></td>
      <td>0</td>
      <td>doc
        <br>xls
        <br>ppt
        <br>msg</td>
      <td>Compound File Binary Format, a container format used for document by older versions of Microsoft Office. It is however an open format used by other programs as well.</td></tr>
    <tr>
      <td>
        <pre>64 65 78 0A 30 33 <br>35 00</pre></td>
      <td>
        <pre>dex.035.</pre></td>
      <td>0</td>
      <td>dex</td>
      <td>Dalvik Executable</td></tr>
    <tr>
      <td>
        <pre>4B 44 4D</pre></td>
      <td>
        <pre>KDM</pre></td>
      <td>0</td>
      <td>vmdk</td>
      <td>VMDK files</td></tr>
    <tr>
      <td>
        <pre>43 72 32 34</pre></td>
      <td>
        <pre>Cr24</pre></td>
      <td>0</td>
      <td>crx</td>
      <td>Google Chrome extension or packaged app</td></tr>
    <tr>
      <td>
        <pre>41 47 44 33</pre></td>
      <td>
        <pre>AGD3</pre></td>
      <td>0</td>
      <td>fh8</td>
      <td>FreeHand 8 document</td></tr>
    <tr>
      <td>
        <pre>05 07 00 00 42 4F <br>42 4F 05 07 00 00 <br>00 00 00 00 00 00 <br>00 00 00 01</pre></td>
      <td>
        <pre>....BOBO ........ ....</pre></td>
      <td>0</td>
      <td>cwk</td>
      <td>AppleWorks 5 document</td></tr>
    <tr>
      <td>
        <pre>06 07 E1 00 42 4F <br>42 4F 06 07 E1 00 <br>00 00 00 00 00 00 <br>00 00 00 01</pre></td>
      <td>
        <pre>....BOBO ........ ....</pre></td>
      <td>0</td>
      <td>cwk</td>
      <td>AppleWorks 6 document</td></tr>
    <tr>
      <td>
        <pre>45 52 02 00 00 00</pre>
        <pre>8B 45 52 02 00 00 <br>00</pre></td>
      <td>
        <pre>ER....</pre>
        <pre>ãER....</pre></td>
      <td>0</td>
      <td>toast</td>
      <td>Roxio Toast disc image file, also some .dmg-files begin with same bytes</td></tr>
    <tr>
      <td>
        <pre>78 01 73 0D 62 62 <br>60</pre></td>
      <td>
        <pre>x.s.bb`</pre></td>
      <td>0</td>
      <td>dmg</td>
      <td>Apple Disk Image file</td></tr>
    <tr>
      <td>
        <pre>78 61 72 21</pre></td>
      <td>
        <pre>xar!</pre></td>
      <td>0</td>
      <td>xar</td>
      <td>eXtensible ARchive format</td></tr>
    <tr>
      <td>
        <pre>50 4D 4F 43 43 4D <br>4F 43</pre></td>
      <td>
        <pre>PMOCCMOC</pre></td>
      <td>0</td>
      <td>dat</td>
      <td>Windows Files And Settings Transfer Repository
        <p>See also USMT 3.0 (Win XP) and USMT 4.0 (Win 7) User Guides</p>
      </td>
    </tr>
    <tr>
      <td>
        <pre>4E 45 53 1A</pre></td>
      <td>
        <pre>NES</pre></td>
      <td>0</td>
      <td>nes</td>
      <td>Nintendo Entertainment System ROM file</td></tr>
    <tr>
      <td>
        <pre>75 73 74 61 72 00 <br>30 30</pre>
        <pre>75 73 74 61 72 20 <br>20 00</pre></td>
      <td>
        <pre>ustar.00</pre>
        <pre>ustar .</pre></td>
      <td>0x101</td>
      <td>tar</td>
      <td>tar archive</td></tr>
    <tr>
      <td>
        <pre>74 6F 78 33</pre></td>
      <td>
        <pre>TOX</pre></td>
      <td>0</td>
      <td>tox</td>
      <td>Open source portable voxel file</td></tr>
    <tr>
      <td>
        <pre>4D 4C 56 49</pre></td>
      <td>
        <pre>MLVI</pre></td>
      <td>0</td>
      <td>MLV</td>
      <td>Magic Lantern Video file</td></tr>
    <tr>
      <td>
        <pre>44 43 4D 01 50 41 <br>33 30</pre></td>
      <td>
        <pre>DCM PA30</pre></td>
      <td>0</td>
      <td></td>
      <td>Windows Update Binary Delta Compression</td></tr>
    <tr>
      <td>
        <pre>37 7A BC AF 27 1C</pre></td>
      <td>
        <pre>7z¼¯'</pre></td>
      <td>0</td>
      <td>7z</td>
      <td>7-Zip File Format</td></tr>
    <tr>
      <td>
        <pre>1F 8B</pre></td>
      <td>
        <pre>..</pre></td>
      <td>0</td>
      <td>gz
        <br>tar.gz</td>
      <td>GZIP compressed file</td></tr>
    <tr>
      <td>
        <pre>FD 37 7A 58 5A 00 <br>00</pre></td>
      <td>
        <pre>²7zXZ..</pre></td>
      <td>0</td>
      <td>xz
        <br>tar.xz</td>
      <td>XZ compression utility
        <br>using LZMA2 compression</td></tr>
    <tr>
      <td>
        <pre>04 22 4D 18</pre></td>
      <td>
        <pre>."M.</pre></td>
      <td>0</td>
      <td>lz4</td>
      <td>LZ4 Frame Format
        <br>
        <p>Remark: LZ4 block format does not offer any magic bytes.</p>
      </td>
    </tr>
    <tr>
      <td>
        <pre>4D 53 43 46</pre></td>
      <td>
        <pre>MSCF</pre></td>
      <td>0</td>
      <td>cab</td>
      <td>Microsoft Cabinet file</td></tr>
    <tr>
      <td>
        <pre>53 5A 44 44 88 F0 <br>27 33</pre></td>
      <td>
        <pre>SZDD....</pre></td>
      <td>0</td>
      <td>Various. (Replacing the last character of the original filename extension with an underscore, e.g. setup.exe becomes setup.ex_)</td>
      <td>Microsoft compressed file in Quantum format, used prior to Windows XP. File can be decompressed using Extract.exe or Expand.exe distributed with earlier versions of Windows.</td></tr>
    <tr>
      <td>
        <pre>46 4C 49 46</pre></td>
      <td>
        <pre>FLIF</pre></td>
      <td>0</td>
      <td>flif</td>
      <td>Free Lossless Image Format</td></tr>
    <tr>
      <td>
        <pre>1A 45 DF A3</pre></td>
      <td>
        <pre>.Eß£</pre></td>
      <td>0</td>
      <td>mkv
        <br>mka
        <br>mks
        <br>mk3d
        <br>webm</td>
      <td>Matroska media container, including WebM</td></tr>
    <tr>
      <td>
        <pre>4D 49 4C 20</pre></td>
      <td>
        <pre>MIL</pre></td>
      <td>0</td>
      <td>stg</td>
      <td>"SEAN&nbsp;: Session Analysis" Training file. Also used in compatible software "Rpw&nbsp;: Rowperfect for Windows" and "RP3W&nbsp;: ROWPERFECT3 for Windows".</td></tr>
    <tr>
      <td>
        <pre>41 54 26 54 46 4F <br>52 <br>4D&nbsp;??&nbsp;??&nbsp;??&nbsp;?? <br>44 4A 56</pre></td>
      <td>
        <pre>AT&amp;TFORM....DJV</pre></td>
      <td>0</td>
      <td>djvu
        <br>djv</td>
      <td>DjVu document
        <br>The following byte is either
        <code>55</code>(
        <code>U</code>) for single-page or
        <code>4D</code>(
        <code>M</code>) for multi-page documents.</td></tr>
    <tr>
      <td>
        <pre>30 82</pre></td>
      <td>
        <pre>0.</pre></td>
      <td>0</td>
      <td>der</td>
      <td>DER encoded X.509 certificate</td></tr>
    <tr>
      <td>
        <pre>44 49 43 4D</pre></td>
      <td>
        <pre>DICM</pre></td>
      <td>0x80</td>
      <td>dcm</td>
      <td>DICOM Medical File Format</td></tr>
    <tr>
      <td>
        <pre>77 4F 46 46</pre></td>
      <td>
        <pre>wOFF</pre></td>
      <td>0</td>
      <td>woff</td>
      <td>WOFF File Format 1.0</td></tr>
    <tr>
      <td>
        <pre>77 4F 46 32</pre></td>
      <td>
        <pre>wOF2</pre></td>
      <td>0</td>
      <td>woff2</td>
      <td>WOFF File Format 2.0</td></tr>
    <tr>
      <td>
        <pre>3c 3f 78 6d 6c 20</pre></td>
      <td>
        <pre>&lt;?xml</pre></td>
      <td>0</td>
      <td>XML</td>
      <td>eXtensible Markup Language when using the ASCII character encoding</td></tr>
    <tr>
      <td>
        <pre>00 61 73 6d</pre></td>
      <td>
        <pre>.asm</pre></td>
      <td>0</td>
      <td>wasm</td>
      <td>WebAssembly binary format</td></tr>
    <tr>
      <td>
        <pre>cf 84 01</pre></td>
      <td></td>
      <td>0</td>
      <td>lep</td>
      <td>Lepton compressed JPEG image</td></tr>
    <tr>
      <td>
        <pre>43 57 53</pre>
        <pre>46 57 53</pre></td>
      <td>CWS
        <p>FWS</p>
      </td>
      <td>0</td>
      <td>swf</td>
      <td>flash .swf</td></tr>
    <tr>
      <td>
        <pre>21 3C 61 72 63 68 <br>3E</pre></td>
      <td>!&lt;arch&gt;.</td>
      <td>0</td>
      <td>deb</td>
      <td>linux deb file</td></tr>
    <tr>
      <td>
        <pre>52 49 46 <br>46&nbsp;??&nbsp;??&nbsp;??&nbsp;?? <br>57 45 42 50</pre></td>
      <td>RIFF....
        <p>WEBP</p>
      </td>
      <td>0</td>
      <td>webp</td>
      <td>Google WebP image file, where&nbsp;??&nbsp;??&nbsp;??&nbsp;?? is the file size. More informarion on WebP File Header</td></tr>
    <tr>
      <td>
        <pre>27 05 19 56</pre></td>
      <td>
        <pre>'..V</pre></td>
      <td>0</td>
      <td></td>
      <td>U-Boot / uImage. Das U-Boot Universal Boot Loader.</td></tr>
    <tr>
      <td>
        <pre>7B 5C 72 74 66 31</pre></td>
      <td>
        <pre>{\rtf1</pre></td>
      <td>0</td>
      <td>rtf</td>
      <td>Rich Text Format</td></tr>
    <tr>
      <td>
        <pre>54 41 50 45</pre></td>
      <td>
        <pre>TAPE</pre></td>
      <td>0</td>
      <td></td>
      <td>Microsoft Tape Format</td></tr>
    <tr>
      <td>
        <pre>47</pre></td>
      <td>
        <pre>G</pre></td>
      <td>0
        <p>0xBC</p>
        <p>0x178</p>
        <p>...</p>
        <p>(every 188th byte)</p>
      </td>
      <td>ts
        <p>tsv</p>
        <p>tsa</p>
      </td>
      <td>MPEG Transport Stream (MPEG-2 Part 1)</td></tr>
    <tr>
      <td>
        <pre>00 00 01 BA</pre></td>
      <td>
        <pre>....</pre></td>
      <td>0</td>
      <td>m2p
        <p>vob</p>
      </td>
      <td>MPEG Program Stream (MPEG-1 Part 1 (essentially identical) and MPEG-2 Part 1)</td></tr>
    <tr>
      <td>
        <pre>00 00 01 BA</pre>
        <pre>47</pre>
        <pre>00 00 01 B3</pre></td>
      <td>
        <pre>....</pre>
        <pre>G</pre>
        <pre>....</pre></td>
      <td>0</td>
      <td>mpg
        <p>mpeg</p>
      </td>
      <td>
        <p>MPEG Program Stream</p>
        <p>MPEG Transport Stream</p>
        <p>MPEG-1 video and MPEG-2 video (MPEG-1 Part 2 and MPEG-2 Part 2)</p>
      </td>
    </tr>
    <tr>
      <td>
        <pre>78 01</pre>
        <pre>78 9C</pre>
        <pre>78 DA</pre></td>
      <td>
        <pre>....</pre></td>
      <td>0</td>
      <td>zlib</td>
      <td>
        <p>No Compression/low</p>
        <p>Default Compression</p>
        <p>Best Compression</p>
      </td>
    </tr>
    <tr>
      <td>
        <pre>62 76 78 32</pre></td>
      <td>
        <pre>bvx2</pre></td>
      <td>0</td>
      <td>lzfse</td>
      <td>LZFSE - Lempel-Ziv style data compression algorithm using Finite State Entropy coding. OSS by Apple.</td></tr>
    <tr>
      <td>
        <pre>4F 52 43</pre></td>
      <td>
        <pre>ORC</pre></td>
      <td>0</td>
      <td>orc</td>
      <td>Apache ORC (Optimized Row Columnar) file format</td></tr>
    <tr>
      <td>
        <pre>4F 62 6A 01</pre></td>
      <td>
        <pre>Obj.</pre></td>
      <td>0</td>
      <td>avro</td>
      <td>Apache Avro binary file format</td></tr>
    <tr>
      <td>
        <pre>53 45 51 36</pre></td>
      <td>
        <pre>SEQ6</pre></td>
      <td>0</td>
      <td>rc</td>
      <td>RCFile columnar file format</td></tr>
    <tr>
      <td>
        <pre>65 87 78 56</pre></td>
      <td>
        <pre>e.xV</pre></td>
      <td>0</td>
      <td>
        <p>p25</p>
        <p>obt</p>
      </td>
      <td>PhotoCap Object Templates</td></tr>
    <tr>
      <td>
        <pre>55 55 aa aa</pre></td>
      <td>
        <pre>UU¬¬</pre></td>
      <td>0</td>
      <td>pcv</td>
      <td>PhotoCap Vector</td></tr>
    <tr>
      <td>
        <pre>78 56 34</pre></td>
      <td>
        <pre>xV4</pre></td>
      <td>0</td>
      <td>
        <p>pbt</p>
        <p>pdt</p>
        <p>pea</p>
        <p>peb</p>
        <p>pet</p>
        <p>pgt</p>
        <p>pict</p>
        <p>pjt</p>
        <p>pkt</p>
        <p>pmt</p>
      </td>
      <td>PhotoCap Template</td></tr>
    <tr>
      <td>
        <pre>50 41 52 31</pre></td>
      <td>
        <pre>PAR1</pre></td>
      <td>0</td>
      <td></td>
      <td>Apache Parquet columnar file format</td></tr>
    <tr>
      <td>
        <pre>45 4D 58 32</pre></td>
      <td>
        <pre>EMX2</pre></td>
      <td>0</td>
      <td>ez2</td>
      <td>Emulator Emaxsynth samples</td></tr>
    <tr>
      <td>
        <pre>45 4D 55 33</pre></td>
      <td>
        <pre>EMU3</pre></td>
      <td>0</td>
      <td>ez3
        <p>iso</p>
      </td>
      <td>Emulator III synth samples</td></tr>
    <tr>
      <td>
        <pre>1B 4C 75 61</pre></td>
      <td>
        <pre>.Lua</pre></td>
      <td>0</td>
      <td>luac</td>
      <td>Lua bytecode</td></tr>
    <tr>
      <td>
        <pre>62 6F 6F 6B 00 00 <br>00 00 6D 61 72 6B <br>00 00 00 00</pre></td>
      <td>
        <pre>book....mark....</pre></td>
      <td>0</td>
      <td>alias</td>
      <td>macOS file Alias (Symbolic link)</td></tr>
    <tr>
      <td>
        <pre>5B 5A 6F 6E 65 54 <br>72 61 6E 73 66 65 <br>72 5D</pre></td>
      <td>
        <pre>[ZoneTransfer]</pre></td>
      <td>0</td>
      <td>Identifier</td>
      <td>Microsoft Zone Identifier for URL Security Zones</td></tr>
    <tr>
      <td>
        <pre>52 65 63 65 69 76 <br>65 64</pre></td>
      <td>
        <pre>Received:</pre></td>
      <td>0</td>
      <td>eml</td>
      <td>Email Message var5</td></tr>
    <tr>
      <td>
        <pre>20 02 01 62 A0 1E <br>AB 07 02 00 00 00</pre></td>
      <td>
        <pre>..b&nbsp;.«.....</pre></td>
      <td>0</td>
      <td>tde</td>
      <td>Tableau Datasource</td></tr>
    <tr>
      <td>
        <pre>37 48 03 02 00 00 <br>00 00 58 35 30 39 <br>4B 45 59</pre></td>
      <td>
        <pre>7H......X509KEY</pre></td>
      <td>0</td>
      <td>kdb</td>
      <td>KDB file</td></tr>
    <tr>
      <td>
        <pre>28 B5 2F FD</pre></td>
      <td>
        <pre>(µ/ý</pre></td>
      <td>0</td>
      <td>zst</td>
      <td>Zstandard compressed file</td></tr>
    <tr>
      <td>
        <pre>3A 29 0A</pre></td>
      <td>
        <pre>:).</pre></td>
      <td>0</td>
      <td>sml</td>
      <td>Smile file</td></tr>
  </tbody>
  <tfoot></tfoot>
</table>