SearchTool.ext是一个提取代码中的用双引号括起来中文，用Lua中的GAME->GetGameTxt(i)替换代码输出到输出路径，中文提取到输出路径的chinese.txt文件中。如果要修改替换字符串，可自行修改tool.lua文件中：

local newstr = string.gsub(str,'"%s-[^"]-[\161-\254]+[^"]-%s-"',
			function(x)
				filetotxt:write(string.format("%d\t%s\n",i+1,string.sub(x,2,-2)));
				i=i+1;
				return string.format("GAMETXT->GetGameTxt(%d)",i)
				end );

