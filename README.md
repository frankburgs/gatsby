
```mermaid

flowchart LR;
  root("#47;root#47;")
  root -.- fi

  subgraph rootw[" "] %% root wrapper
    direction TB

    subgraph fi[" "] %% root files
      direction LR
      f01(.babelrc) -.- f02(eslintignore) -.-f03(.gitignore) -.- 
    	f04(.prettierignore) -.- f05(.prettierrc) -.-f06( Dockerfile) -.- f07(LICENSE) -.- yml01(docker-compose) -.- js01(gatsby-browser) -.- js02(gatsby-config) -.- js03(gatsby-node) -.- js04(gatsby-ssr) -.- jsn01(.eslintrc) -.- jsn02(package) -.- md01(README) -.- lck01(yarn)
      linkStyle 1,2,3,4,5,6,7,8,9,10,11,12,13,14,15 stroke:#000
   end

    subgraph fo01[" "] %% root/.vscode/
    direction LR;
      01("#47;.vscode#47;")
      subgraph 01fi
      direction LR;
      end
      01 -.- 01fi
    end

    subgraph fo02[" "] %% root/bin/
      02("#47;bin#47;")
      subgraph 02fi %% root/bin files
      direction LR;
      end
    end

    subgraph fo03[" "] %% root/chart/
      03("#47;chart#47;")
    end

    subgraph fo04[" "] %% root/config/
      04("#47;config#47;")
    end

    subgraph fo05[" "] %% root/ops/
      05("#47;ops#47;")
    end

    subgraph fo06[" "] %% root/src/
      06("#47;src#47;")
    end

    subgraph fo07[" "] %% root/static/
      07("#47;static#47;")
    end
  end %% End root subgraph

  root -.- fo01 & fo02 & fo03 & fo04 & fo05 & fo06 & fo07
   linkStyle 16,17,18,19,20,21,22 stroke:#00ffff,stroke-dasharray: 5 5


```
