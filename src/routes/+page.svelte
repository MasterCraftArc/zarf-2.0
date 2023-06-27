<script>
    import Card from '../components/Card.svelte';
    import Home from '../components/Home/Home.svelte';
    import Navbar from '../components/Navbar/Navbar.svelte'
    import Blob from '../components/blob/Blob.svelte';
    import webSecure from '../assets/png/cloud-icons/web-security.png'
    import '../styles/global.css'
    import wireLessCloud from '../assets/png/cloud-icons/wireless-cloud.png'
    import server from '../assets/png/cloud-icons/server.png'
	import Columns from '../components/Columns/Columns.svelte';
import rocket from '../assets/png/zarf-rocket.png'
import nuclear from '../assets/png/zarf-nuclear.png'
import Column from '../components/Columns/Column.svelte';
import sub from '../assets/png/zarf-sub.png'
import Cards from '../components/Cards.svelte'
import community from '../assets/png/cloud-icons/community.png'
import hosting from '../assets/png/cloud-icons/hosting.png'
import pieces from '../assets/png/cloud-icons/pieces.png'
import document from '../assets/png/cloud-icons/document.png'
	import StatsCard from '../components/statsCard/StatsCard.svelte';
	import Footer from '../components/footer/Footer.svelte';
</script>

<Navbar/>

<div class="blob"><Blob/></div>
<Home/>
<div class="cardHolder">
  <div class="Cards">
    <Card img={webSecure} heroText='Securely Package
    Apps & Resources' text="Provides the ability to package a chunk of the internet and then securely deliver all of the files and dependencies needed to run an application in a disconnected environment."/>

    <Card img={wireLessCloud} heroText='Deploy Cloud Apps
    While Disconnected' text='Provides the ability to deploy apps declaratively and without internet connectivity. Opening up the door for modern cloud capabilities to be deployed in disconnected environments.'/>

    <Card img={server} heroText='Easily Maintain Apps
    While Disconnected
    ' text='Zarf reduces the skill and resources needed to manage and update applications in disconnected environments, ensuring no down time or data loss when updating software.'/>
  </div>
  </div>

  <Blob/>
  <Columns HeroText='Sometimes Disconnected' text='Some systems experience disconnection occasionally due to temporary loss of access, like a rocket going around the moon. Zarf keeps those systems running.' img={rocket}/>

  <Column HeroText='Sometimes Disconnected' text='Some systems experience disconnection occasionally due to temporary loss of access, like a rocket going around the moon. Zarf keeps those systems running.' img={sub}/>

  <Columns HeroText='Disconnected in Emergencies' text='The worlds most important infrastructure needs to be able to control their connection to the internet and still run in the case of internet loss or a cyber attack.' img={nuclear}/>

  <div class="CardsContainer">
  <div class="Cards">

    <Cards img={community} heroText='Free and Open
    Source Solution' text="Source code is open and viewable to the public which increases security through transparency. Zarf is also a free tool and available for public use."/>
    <Cards img={hosting} heroText='Built to Be Distro
    Agnostic' text="Currently offers fully automated support for K3s, K3d, and Kind. Is also compatible with EKS, AKS, GKE, RKE2 and many others distro services."/>
    <Cards img={pieces} heroText='Automates SBOM
    Creation' text="Automatically generates an SBOM from the images listed within a package, in compliance with federal mandate. Includes a UI for SBOM viewing."/>
  </div>

  <div class="Cards">
    <Cards img={document} heroText='Installs Packages
    with Two Commands' text="Reduces the risk of installation error and complexity of installation procedures by simplifying the installation of packages to just two steps."/>
    <Cards img={hosting} heroText='Consistently Deploy
    Across Environments' text="Ensures that applications are deployed the same way each time, whether deployed to a different cluster, machine or environment."/>
    <Cards img={document} heroText='Host Registry
    & Git Server' text="Zarf spins up K8 clusters, docker registries and git servers offline to allow for disconnected use. For connected users this provides a fail over solution."/>
  </div>
</div>
<StatsCard/>
<Blob/>
<Footer/>
<style>
      .blob {
    position: absolute;
    top: -40px;
    left: -20%;
    width: 100%;
    height: 100%;
    z-index: 0;
    background: var(--gradient-background);
  }

  .Cards{
            display: flex;
            align-items: center;
            justify-content: space-evenly;
            flex-wrap: wrap;
        }


</style>
