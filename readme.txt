SearchTool.ext��һ����ȡ�����е���˫�������������ģ���Lua�е�GAME->GetGameTxt(i)�滻������������·����������ȡ�����·����chinese.txt�ļ��С����Ҫ�޸��滻�ַ������������޸�tool.lua�ļ��У�

local newstr = string.gsub(str,'"%s-[^"]-[\161-\254]+[^"]-%s-"',
			function(x)
				filetotxt:write(string.format("%d\t%s\n",i+1,string.sub(x,2,-2)));
				i=i+1;
				return string.format("GAMETXT->GetGameTxt(%d)",i)
				end );

